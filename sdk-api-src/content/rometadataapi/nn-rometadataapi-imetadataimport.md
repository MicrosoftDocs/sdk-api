---
UID: NN:rometadataapi.IMetaDataImport
title: IMetaDataImport (rometadataapi.h)
description: Provides methods for importing and manipulating existing metadata from a portable executable (PE) file or other source, such as a type library or a stand-alone, run-time metadata binary.
helpviewer_keywords: ["IMetaDataImport","IMetaDataImport interface [Windows Runtime]","IMetaDataImport interface [Windows Runtime]","described","rometadataapi/IMetaDataImport","winrt.imetadataimport"]
old-location: winrt\imetadataimport.htm
tech.root: WinRT
ms.assetid: 5457d9d3-9a43-4e89-a52f-1254662ed92a
ms.date: 12/05/2018
ms.keywords: IMetaDataImport, IMetaDataImport interface [Windows Runtime], IMetaDataImport interface [Windows Runtime],described, rometadataapi/IMetaDataImport, winrt.imetadataimport
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMetaDataImport
 - rometadataapi/IMetaDataImport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport
---

# IMetaDataImport interface


## -description

Provides methods for importing and manipulating existing metadata from a portable executable (PE) file or other source, such as a type library or a stand-alone, run-time metadata binary.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataImport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMetaDataImport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataImport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-closeenum">CloseEnum</a>
</td>
<td align="left" width="63%">
Closes the enumerator that is identified by the specified handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-countenum">CountEnum</a>
</td>
<td align="left" width="63%">
Gets the number of elements in the enumeration that was retrieved by the specified enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumcustomattributes">EnumCustomAttributes</a>
</td>
<td align="left" width="63%">
Enumerates custom attribute-definition tokens associated with the specified type or member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumevents">EnumEvents</a>
</td>
<td align="left" width="63%">
Enumerates event definition tokens for the specified TypeDef token.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumfields">EnumFields</a>
</td>
<td align="left" width="63%">
Enumerates FieldDef tokens for the type referenced by the specified TypeDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumfieldswithname">EnumFieldsWithName</a>
</td>
<td align="left" width="63%">
Enumerates FieldDef tokens of the specified type with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enuminterfaceimpls">EnumInterfaceImpls</a>
</td>
<td align="left" width="63%">
Enumerates MethodDef tokens representing interface implementations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummemberrefs">EnumMemberRefs</a>
</td>
<td align="left" width="63%">
Enumerates MemberRef tokens representing members of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummembers">EnumMembers</a>
</td>
<td align="left" width="63%">
Enumerates MemberDef tokens representing members of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummemberswithname">EnumMembersWithName</a>
</td>
<td align="left" width="63%">
Enumerates MemberDef tokens representing members of the specified type with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummethodimpls">EnumMethodImpls</a>
</td>
<td align="left" width="63%">
Enumerates MethodBody and MethodDeclaration tokens representing methods of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummethods">EnumMethods</a>
</td>
<td align="left" width="63%">
Enumerates MethodDef tokens representing methods of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummethodsemantics">EnumMethodSemantics</a>
</td>
<td align="left" width="63%">
Enumerates the properties and the property-change events to which the specified method is related.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummethodswithname">EnumMethodsWithName</a>
</td>
<td align="left" width="63%">
Enumerates methods that have the specified name and that are defined by the type referenced by the specified TypeDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummodulerefs">EnumModuleRefs</a>
</td>
<td align="left" width="63%">
Enumerates ModuleRef tokens that represent imported modules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumparams">EnumParams</a>
</td>
<td align="left" width="63%">
Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumpermissionsets">EnumPermissionSets</a>
</td>
<td align="left" width="63%">
Enumerates permissions for the objects in a specified metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumproperties">EnumProperties</a>
</td>
<td align="left" width="63%">
Enumerates PropertyDef tokens representing the properties of the type referenced by the specified TypeDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumsignatures">EnumSignatures</a>
</td>
<td align="left" width="63%">
Enumerates Signature tokens representing stand-alone signatures in the current scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumtypedefs">EnumTypeDefs</a>
</td>
<td align="left" width="63%">
Enumerates TypeDef tokens representing all types within the current scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumtyperefs">EnumTypeRefs</a>
</td>
<td align="left" width="63%">
Enumerates TypeRef tokens defined in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumtypespecs">EnumTypeSpecs</a>
</td>
<td align="left" width="63%">
Enumerates TypeSpec tokens defined in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumunresolvedmethods">EnumUnresolvedMethods</a>
</td>
<td align="left" width="63%">
Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumuserstrings">EnumUserStrings</a>
</td>
<td align="left" width="63%">
Enumerates String tokens representing hard-coded strings in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-findmemberref">FindMemberRef</a>
</td>
<td align="left" width="63%">
Gets a pointer to the MemberRef token for the member reference that is enclosed by the specified Type and that has the specified name and metadata signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-findtypedefbyname">FindTypeDefByName</a>
</td>
<td align="left" width="63%">
Gets a pointer to the TypeDef metadata token for the Type with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-findtyperef">FindTypeRef</a>
</td>
<td align="left" width="63%">
Gets a pointer to the TypeRef token for the Type reference that is in the specified scope and that has the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getcustomattributebyname">GetCustomAttributeByName</a>
</td>
<td align="left" width="63%">
Gets the custom attribute, given its name and owner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getcustomattributeprops">GetCustomAttributeProps</a>
</td>
<td align="left" width="63%">
Gets the value of the custom attribute, given its metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getfieldmarshal">GetFieldMarshal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the native, unmanaged type of the field represented by the specified field metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getfieldprops">GetFieldProps</a>
</td>
<td align="left" width="63%">
Gets metadata associated with the field referenced by the specified FieldDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getinterfaceimplprops">GetInterfaceImplProps</a>
</td>
<td align="left" width="63%">
Gets a pointer to the metadata tokens for the Type that implements the specified method, and for the interface that declares that method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getmemberprops">GetMemberProps</a>
</td>
<td align="left" width="63%">
Gets metadata information, including the name, binary signature, and relative virtual address, of the Type member referenced by the specified metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getmemberrefprops">GetMemberRefProps</a>
</td>
<td align="left" width="63%">
Gets metadata associated with the member referenced by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getmethodprops">GetMethodProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the method referenced by the specified MethodDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getmethodsemantics">GetMethodSemantics</a>
</td>
<td align="left" width="63%">
Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getmodulefromscope">GetModuleFromScope</a>
</td>
<td align="left" width="63%">
Gets a metadata token for the module referenced in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getmodulerefprops">GetModuleRefProps</a>
</td>
<td align="left" width="63%">
Gets the name of the module referenced by the specified metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getnamefromtoken">GetNameFromToken</a>
</td>
<td align="left" width="63%">
Gets the UTF-8 name of the object referenced by the specified metadata token. This method is obsolete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getnativecallconvfromsig">GetNativeCallConvFromSig</a>
</td>
<td align="left" width="63%">
Gets the native calling convention for the method that is represented by the specified signature pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getnestedclassprops">GetNestedClassProps</a>
</td>
<td align="left" width="63%">
Gets the TypeDef token for the parent Type of the specified nested type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/hh870628(v=vs.85)">GetParamForMethodIndex</a>
</td>
<td align="left" width="63%">
Gets the token that represents a specified parameter of the method represented by the specified MethodDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getparamprops">GetParamProps</a>
</td>
<td align="left" width="63%">
Gets metadata values for the parameter referenced by the specified ParamDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getpermissionsetprops">GetPermissionSetProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the System.Security.PermissionSet represented by the specified Permission token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getpinvokemap">GetPinvokeMap</a>
</td>
<td align="left" width="63%">
Gets a ModuleRef token to represent the target assembly of a PInvoke call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getrva">GetRVA</a>
</td>
<td align="left" width="63%">
Gets the relative virtual address (RVA) and the implementation flags of the method or field represented by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getscopeprops">GetScopeProps</a>
</td>
<td align="left" width="63%">
Gets the name and optionally the version identifier of the assembly or module in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getsigfromtoken">GetSigFromToken</a>
</td>
<td align="left" width="63%">
Gets the binary metadata signature associated with the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-gettypedefprops">GetTypeDefProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the Type referenced by the specified TypeRef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-gettyperefprops">GetTypeRefProps</a>
</td>
<td align="left" width="63%">
Returns metadata information for the Type represented by the specified TypeDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-gettypespecfromtoken">GetTypeSpecFromToken</a>
</td>
<td align="left" width="63%">
Gets the binary metadata signature of the type specification represented by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-getuserstring">GetUserString</a>
</td>
<td align="left" width="63%">
Gets the literal string represented by the specified metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-isglobal">IsGlobal</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the field, method, or type represented by the specified metadata token has global scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-isvalidtoken">IsValidToken</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the specified token holds a valid reference to a code object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-resetenum">ResetEnum</a>
</td>
<td align="left" width="63%">
Resets the specified enumerator to the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-resolvetyperef">ResolveTypeRef</a>
</td>
<td align="left" width="63%">
Resolves a Type reference represented by the specified TypeRef token.

</td>
</tr>
</table>