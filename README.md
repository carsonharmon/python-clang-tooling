# python-clang-tooling

```python
from libtooling import *

def fn_finder_cb(nodes):
    if nodes.getFunctionDecl("0"):
        print("print function found")

def int_finder_cb(nodes):
    if nodes.getVarDecl("int"):
        print("integer found")

fn_finder1 = functionDecl(hasName("print")).bind("0")
int_finder = varDecl(hasType(isInteger())).bind("int")

tooling = Tooling("../tests/simple.cc")

tooling.add(fn_finder1, fn_finder_cb)
tooling.add(int_finder, int_finder_cb)

tooling.run()
```

# Node Matchers

Return Type | Name | Parameters | Implemented
------------ | ------------- | ------------- | -------------
Matcher\<CXXCtorInitializer\> | cxxCtorInitializer | Matcher<CXXCtorInitializer>| 
Matcher<Decl> | accessSpecDecl | Matcher<AccessSpecDecl>| 
Matcher<Decl> | blockDecl | Matcher<BlockDecl>| 
Matcher<Decl> | classTemplateDecl | Matcher<ClassTemplateDecl>| 
Matcher<Decl> | classTemplatePartialSpecializationDecl | Matcher<ClassTemplatePartialSpecializationDecl>| 
Matcher<Decl> | classTemplateSpecializationDecl | Matcher<ClassTemplateSpecializationDecl>| 
Matcher<Decl> | cxxConstructorDecl | Matcher<CXXConstructorDecl>| 
Matcher<Decl> | cxxConversionDecl | Matcher<CXXConversionDecl>| 
Matcher<Decl> | cxxDestructorDecl | Matcher<CXXDestructorDecl>| 
Matcher<Decl> | cxxMethodDecl | Matcher<CXXMethodDecl>| 
Matcher<Decl> | cxxRecordDecl | Matcher<CXXRecordDecl>| 
Matcher<Decl> | decl | Matcher<Decl>| 
Matcher<Decl> | declaratorDecl | Matcher<DeclaratorDecl>| 
Matcher<Decl> | enumConstantDecl | Matcher<EnumConstantDecl>| 
Matcher<Decl> | enumDecl | Matcher<EnumDecl>| 
Matcher<Decl> | fieldDecl | Matcher<FieldDecl>| 
Matcher<Decl> | friendDecl | Matcher<FriendDecl>| 
Matcher<Decl> | functionDecl | Matcher<FunctionDecl>| 
Matcher<Decl> | functionTemplateDecl | Matcher<FunctionTemplateDecl>| 
Matcher<Decl> | indirectFieldDecl | Matcher<IndirectFieldDecl>| 
Matcher<Decl> | labelDecl | Matcher<LabelDecl>| 
Matcher<Decl> | linkageSpecDecl | Matcher<LinkageSpecDecl>| 
Matcher<Decl> | namedDecl | Matcher<NamedDecl>| 
Matcher<Decl> | namespaceAliasDecl | Matcher<NamespaceAliasDecl>| 
Matcher<Decl> | namespaceDecl | Matcher<NamespaceDecl>| 
Matcher<Decl> | nonTypeTemplateParmDecl | Matcher<NonTypeTemplateParmDecl>| 
Matcher<Decl> | objcCategoryDecl | Matcher<ObjCCategoryDecl>| 
Matcher<Decl> | objcCategoryImplDecl | Matcher<ObjCCategoryImplDecl>| 
Matcher<Decl> | objcImplementationDecl | Matcher<ObjCImplementationDecl>| 
Matcher<Decl> | objcInterfaceDecl | Matcher<ObjCInterfaceDecl>| 
Matcher<Decl> | objcIvarDecl | Matcher<ObjCIvarDecl>| 
Matcher<Decl> | objcMethodDecl | Matcher<ObjCMethodDecl>| 
Matcher<Decl> | objcPropertyDecl | Matcher<ObjCPropertyDecl>| 
Matcher<Decl> | objcProtocolDecl | Matcher<ObjCProtocolDecl>| 
Matcher<Decl> | parmVarDecl | Matcher<ParmVarDecl>| 
Matcher<Decl> | recordDecl | Matcher<RecordDecl>| 
Matcher<Decl> | staticAssertDecl | Matcher<StaticAssertDecl>| 
Matcher<Decl> | templateTypeParmDecl | Matcher<TemplateTypeParmDecl>| 
Matcher<Decl> | translationUnitDecl | Matcher<TranslationUnitDecl>| 
Matcher<Decl> | typeAliasDecl | Matcher<TypeAliasDecl>| 
Matcher<Decl> | typeAliasTemplateDecl | Matcher<TypeAliasTemplateDecl>| 
Matcher<Decl> | typedefDecl | Matcher<TypedefDecl>| 
Matcher<Decl> | typedefNameDecl | Matcher<TypedefNameDecl>| 
Matcher<Decl> | unresolvedUsingTypenameDecl | Matcher<UnresolvedUsingTypenameDecl>| 
Matcher<Decl> | unresolvedUsingValueDecl | Matcher<UnresolvedUsingValueDecl>| 
Matcher<Decl> | usingDecl | Matcher<UsingDecl>| 
Matcher<Decl> | usingDirectiveDecl | Matcher<UsingDirectiveDecl>| 
Matcher<Decl> | valueDecl | Matcher<ValueDecl>| 
Matcher<Decl> | varDecl | Matcher<VarDecl>| 
Matcher<NestedNameSpecifierLoc> | nestedNameSpecifierLoc | Matcher<NestedNameSpecifierLoc>| 
Matcher<NestedNameSpecifier> | nestedNameSpecifier | Matcher<NestedNameSpecifier>| 
Matcher<OMPClause> | ompDefaultClause | Matcher<OMPDefaultClause>| 
Matcher<QualType> | qualType | Matcher<QualType>| 
Matcher<Stmt> | addrLabelExpr | Matcher<AddrLabelExpr>| 
Matcher<Stmt> | arraySubscriptExpr | Matcher<ArraySubscriptExpr>| 
Matcher<Stmt> | asmStmt | Matcher<AsmStmt>| 
Matcher<Stmt> | atomicExpr | Matcher<AtomicExpr>| 
Matcher<Stmt> | autoreleasePoolStmt | Matcher<ObjCAutoreleasePoolStmt>| 
Matcher<Stmt> | binaryConditionalOperator | Matcher<BinaryConditionalOperator>| 
Matcher<Stmt> | binaryOperator | Matcher<BinaryOperator>| 
Matcher<Stmt> | blockExpr | Matcher<BlockExpr>| 
Matcher<Stmt> | breakStmt | Matcher<BreakStmt>| 
Matcher<Stmt> | cStyleCastExpr | Matcher<CStyleCastExpr>| 
Matcher<Stmt> | callExpr | Matcher<CallExpr>| 
Matcher<Stmt> | caseStmt | Matcher<CaseStmt>| 
Matcher<Stmt> | castExpr | Matcher<CastExpr>| 
Matcher<Stmt> | characterLiteral | Matcher<CharacterLiteral>| 
Matcher<Stmt> | chooseExpr | Matcher<ChooseExpr>| 
Matcher<Stmt> | compoundLiteralExpr | Matcher<CompoundLiteralExpr>| 
Matcher<Stmt> | compoundStmt | Matcher<CompoundStmt>| 
Matcher<Stmt> | conditionalOperator | Matcher<ConditionalOperator>| 
Matcher<Stmt> | constantExpr | Matcher<ConstantExpr>| 
Matcher<Stmt> | continueStmt | Matcher<ContinueStmt>| 
Matcher<Stmt> | cudaKernelCallExpr | Matcher<CUDAKernelCallExpr>| 
Matcher<Stmt> | cxxBindTemporaryExpr | Matcher<CXXBindTemporaryExpr>| 
Matcher<Stmt> | cxxBoolLiteral | Matcher<CXXBoolLiteralExpr>| 
Matcher<Stmt> | cxxCatchStmt | Matcher<CXXCatchStmt>| 
Matcher<Stmt> | cxxConstCastExpr | Matcher<CXXConstCastExpr>| 
Matcher<Stmt> | cxxConstructExpr | Matcher<CXXConstructExpr>| 
Matcher<Stmt> | cxxDefaultArgExpr | Matcher<CXXDefaultArgExpr>| 
Matcher<Stmt> | cxxDeleteExpr | Matcher<CXXDeleteExpr>| 
Matcher<Stmt> | cxxDependentScopeMemberExpr | Matcher<CXXDependentScopeMemberExpr>| 
Matcher<Stmt> | cxxDynamicCastExpr | Matcher<CXXDynamicCastExpr>| 
Matcher<Stmt> | cxxForRangeStmt | Matcher<CXXForRangeStmt>| 
Matcher<Stmt> | cxxFunctionalCastExpr | Matcher<CXXFunctionalCastExpr>| 
Matcher<Stmt> | cxxMemberCallExpr | Matcher<CXXMemberCallExpr>| 
Matcher<Stmt> | cxxNewExpr | Matcher<CXXNewExpr>| 
Matcher<Stmt> | cxxNullPtrLiteralExpr | Matcher<CXXNullPtrLiteralExpr>| 
Matcher<Stmt> | cxxOperatorCallExpr | Matcher<CXXOperatorCallExpr>| 
Matcher<Stmt> | cxxReinterpretCastExpr | Matcher<CXXReinterpretCastExpr>| 
Matcher<Stmt> | cxxStaticCastExpr | Matcher<CXXStaticCastExpr>| 
Matcher<Stmt> | cxxStdInitializerListExpr | Matcher<CXXStdInitializerListExpr>| 
Matcher<Stmt> | cxxTemporaryObjectExpr | Matcher<CXXTemporaryObjectExpr>| 
Matcher<Stmt> | cxxThisExpr | Matcher<CXXThisExpr>| 
Matcher<Stmt> | cxxThrowExpr | Matcher<CXXThrowExpr>| 
Matcher<Stmt> | cxxTryStmt | Matcher<CXXTryStmt>| 
Matcher<Stmt> | cxxUnresolvedConstructExpr | Matcher<CXXUnresolvedConstructExpr>| 
Matcher<Stmt> | declRefExpr | Matcher<DeclRefExpr>| 
Matcher<Stmt> | declStmt | Matcher<DeclStmt>| 
Matcher<Stmt> | defaultStmt | Matcher<DefaultStmt>| 
Matcher<Stmt> | designatedInitExpr | Matcher<DesignatedInitExpr>| 
Matcher<Stmt> | doStmt | Matcher<DoStmt>| 
Matcher<Stmt> | explicitCastExpr | Matcher<ExplicitCastExpr>| 
Matcher<Stmt> | expr | Matcher<Expr>| 
Matcher<Stmt> | exprWithCleanups | Matcher<ExprWithCleanups>| 
Matcher<Stmt> | floatLiteral | Matcher<FloatingLiteral>| 
Matcher<Stmt> | forStmt | Matcher<ForStmt>| 
Matcher<Stmt> | gnuNullExpr | Matcher<GNUNullExpr>| 
Matcher<Stmt> | gotoStmt | Matcher<GotoStmt>| 
Matcher<Stmt> | ifStmt | Matcher<IfStmt>| 
Matcher<Stmt> | imaginaryLiteral | Matcher<ImaginaryLiteral>| 
Matcher<Stmt> | implicitCastExpr | Matcher<ImplicitCastExpr>| 
Matcher<Stmt> | implicitValueInitExpr | Matcher<ImplicitValueInitExpr>| 
Matcher<Stmt> | initListExpr | Matcher<InitListExpr>| 
Matcher<Stmt> | integerLiteral | Matcher<IntegerLiteral>| 
Matcher<Stmt> | labelStmt | Matcher<LabelStmt>| 
Matcher<Stmt> | lambdaExpr | Matcher<LambdaExpr>| 
Matcher<Stmt> | materializeTemporaryExpr | Matcher<MaterializeTemporaryExpr>| 
Matcher<Stmt> | memberExpr | Matcher<MemberExpr>| 
Matcher<Stmt> | nullStmt | Matcher<NullStmt>| 
Matcher<Stmt> | objcCatchStmt | Matcher<ObjCAtCatchStmt>| 
Matcher<Stmt> | objcFinallyStmt | Matcher<ObjCAtFinallyStmt>| 
Matcher<Stmt> | objcIvarRefExpr | Matcher<ObjCIvarRefExpr>| 
Matcher<Stmt> | objcMessageExpr | Matcher<ObjCMessageExpr>| 
Matcher<Stmt> | objcThrowStmt | Matcher<ObjCAtThrowStmt>| 
Matcher<Stmt> | objcTryStmt | Matcher<ObjCAtTryStmt>| 
Matcher<Stmt> | ompExecutableDirective | Matcher<OMPExecutableDirective>| 
Matcher<Stmt> | opaqueValueExpr | Matcher<OpaqueValueExpr>| 
Matcher<Stmt> | parenExpr | Matcher<ParenExpr>| 
Matcher<Stmt> | parenListExpr | Matcher<ParenListExpr>| 
Matcher<Stmt> | predefinedExpr | Matcher<PredefinedExpr>| 
Matcher<Stmt> | returnStmt | Matcher<ReturnStmt>| 
Matcher<Stmt> | stmt | Matcher<Stmt>| 
Matcher<Stmt> | stmtExpr | Matcher<StmtExpr>| 
Matcher<Stmt> | stringLiteral | Matcher<StringLiteral>| 
Matcher<Stmt> | substNonTypeTemplateParmExpr | Matcher<SubstNonTypeTemplateParmExpr>| 
Matcher<Stmt> | switchCase | Matcher<SwitchCase>| 
Matcher<Stmt> | switchStmt | Matcher<SwitchStmt>| 
Matcher<Stmt> | unaryExprOrTypeTraitExpr | Matcher<UnaryExprOrTypeTraitExpr>| 
Matcher<Stmt> | unaryOperator | Matcher<UnaryOperator>| 
Matcher<Stmt> | unresolvedLookupExpr | Matcher<UnresolvedLookupExpr>| 
Matcher<Stmt> | unresolvedMemberExpr | Matcher<UnresolvedMemberExpr>| 
Matcher<Stmt> | userDefinedLiteral | Matcher<UserDefinedLiteral>| 
Matcher<Stmt> | whileStmt | Matcher<WhileStmt>| 
Matcher<TemplateArgument> | templateArgument | Matcher<TemplateArgument>| 
Matcher<TemplateName> | templateName | Matcher<TemplateName>| 
Matcher<TypeLoc> | typeLoc | Matcher<TypeLoc>| 
Matcher<Type> | arrayType | Matcher<ArrayType>| 
Matcher<Type> | atomicType | Matcher<AtomicType>| 
Matcher<Type> | autoType | Matcher<AutoType>| 
Matcher<Type> | blockPointerType | Matcher<BlockPointerType>| 
Matcher<Type> | builtinType | Matcher<BuiltinType>| 
Matcher<Type> | complexType | Matcher<ComplexType>| 
Matcher<Type> | constantArrayType | Matcher<ConstantArrayType>| 
Matcher<Type> | decayedType | Matcher<DecayedType>| 
Matcher<Type> | decltypeType | Matcher<DecltypeType>| 
Matcher<Type> | dependentSizedArrayType | Matcher<DependentSizedArrayType>| 
Matcher<Type> | elaboratedType | Matcher<ElaboratedType>| 
Matcher<Type> | enumType | Matcher<EnumType>| 
Matcher<Type> | functionProtoType | Matcher<FunctionProtoType>| 
Matcher<Type> | functionType | Matcher<FunctionType>| 
Matcher<Type> | incompleteArrayType | Matcher<IncompleteArrayType>| 
Matcher<Type> | injectedClassNameType | Matcher<InjectedClassNameType>| 
Matcher<Type> | lValueReferenceType | Matcher<LValueReferenceType>| 
Matcher<Type> | memberPointerType | Matcher<MemberPointerType>| 
Matcher<Type> | objcObjectPointerType | Matcher<ObjCObjectPointerType>| 
Matcher<Type> | parenType | Matcher<ParenType>| 
Matcher<Type> | pointerType | Matcher<PointerType>| 
Matcher<Type> | rValueReferenceType | Matcher<RValueReferenceType>| 
Matcher<Type> | recordType | Matcher<RecordType>| 
Matcher<Type> | referenceType | Matcher<ReferenceType>| 
Matcher<Type> | substTemplateTypeParmType | Matcher<SubstTemplateTypeParmType>| 
Matcher<Type> | tagType | Matcher<TagType>| 
Matcher<Type> | templateSpecializationType | Matcher<TemplateSpecializationType>| 
Matcher<Type> | templateTypeParmType | Matcher<TemplateTypeParmType>| 
Matcher<Type> | type | Matcher<Type>| 
Matcher<Type> | typedefType | Matcher<TypedefType>| 
Matcher<Type> | unaryTransformType | Matcher<UnaryTransformType>| 
Matcher<Type> | variableArrayType | Matcher<VariableArrayType>| 
