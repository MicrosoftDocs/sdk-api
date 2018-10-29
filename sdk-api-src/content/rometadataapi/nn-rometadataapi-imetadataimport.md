---
UID: NN:rometadataapi.IMetaDataImport
title: IMetaDataImport
author: windows-sdk-content
description: Provides methods for importing and manipulating existing metadata from a portable executable (PE) file or other source, such as a type library or a stand-alone, run-time metadata binary.
old-location: winrt\imetadataimport.htm
tech.root: WinRT
ms.assetid: 5457d9d3-9a43-4e89-a52f-1254662ed92a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMetaDataImport, IMetaDataImport interface [Windows Runtime], IMetaDataImport interface [Windows Runtime],described, rometadataapi/IMetaDataImport, winrt.imetadataimport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport interface


## -description


Provides methods for importing and manipulating existing metadata from a portable executable (PE) file or other source, such as a type library or a stand-alone, run-time metadata binary.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataImport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMetaDataImport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3495afdf-ca88-4967-b7b3-6320114b9c50">CloseEnum</a>
</td>
<td align="left" width="63%">
Closes the enumerator that is identified by the specified handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67146070-1710-4602-845c-a2a3cd5efdad">CountEnum</a>
</td>
<td align="left" width="63%">
Gets the number of elements in the enumeration that was retrieved by the specified enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5ecb71e-a52f-421b-aab9-48efcc77ec2f">EnumCustomAttributes</a>
</td>
<td align="left" width="63%">
Enumerates custom attribute-definition tokens associated with the specified type or member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/442b5db1-1e5f-4314-9c53-dbd0f0651d3c">EnumEvents</a>
</td>
<td align="left" width="63%">
Enumerates event definition tokens for the specified TypeDef token.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9f8f389-fdb2-404b-a24e-cf2cf119bf55">EnumFields</a>
</td>
<td align="left" width="63%">
Enumerates FieldDef tokens for the type referenced by the specified TypeDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6035f267-778d-4d7d-84eb-1081f33ff619">EnumFieldsWithName</a>
</td>
<td align="left" width="63%">
Enumerates FieldDef tokens of the specified type with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37f3eada-7719-4303-a9c7-57ee396a5dc5">EnumInterfaceImpls</a>
</td>
<td align="left" width="63%">
Enumerates MethodDef tokens representing interface implementations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/900777d4-14fc-4d64-a01c-395f5fafe5e4">EnumMemberRefs</a>
</td>
<td align="left" width="63%">
Enumerates MemberRef tokens representing members of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb1e90fe-e5c8-4f6d-b38a-ae7f46cb34e9">EnumMembers</a>
</td>
<td align="left" width="63%">
Enumerates MemberDef tokens representing members of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfb72609-7db5-4780-aeeb-b3effa37665a">EnumMembersWithName</a>
</td>
<td align="left" width="63%">
Enumerates MemberDef tokens representing members of the specified type with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48df8d5a-8fd2-4b36-9fb1-6f45551c1d37">EnumMethodImpls</a>
</td>
<td align="left" width="63%">
Enumerates MethodBody and MethodDeclaration tokens representing methods of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b0424d8-a0e3-4241-b957-d944e018cb31">EnumMethods</a>
</td>
<td align="left" width="63%">
Enumerates MethodDef tokens representing methods of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b3be5bb-1da7-40d7-8407-c08c2f2723e5">EnumMethodSemantics</a>
</td>
<td align="left" width="63%">
Enumerates the properties and the property-change events to which the specified method is related.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5252b535-23e5-4af1-91df-006717c4e159">EnumMethodsWithName</a>
</td>
<td align="left" width="63%">
Enumerates methods that have the specified name and that are defined by the type referenced by the specified TypeDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd3a8242-0cc9-4199-ada3-de227fe292bd">EnumModuleRefs</a>
</td>
<td align="left" width="63%">
Enumerates ModuleRef tokens that represent imported modules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d3cc66e-575d-4451-bab7-e3dd24fd5060">EnumParams</a>
</td>
<td align="left" width="63%">
Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20fec6e8-02f8-4158-8d61-550653e99dad">EnumPermissionSets</a>
</td>
<td align="left" width="63%">
Enumerates permissions for the objects in a specified metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54b89188-43d3-4997-aef4-48beaae151da">EnumProperties</a>
</td>
<td align="left" width="63%">
Enumerates PropertyDef tokens representing the properties of the type referenced by the specified TypeDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/311cfa18-6eb5-4872-9a46-3c8dcf901f4f">EnumSignatures</a>
</td>
<td align="left" width="63%">
Enumerates Signature tokens representing stand-alone signatures in the current scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64dc7018-721f-4747-b798-fbf70bac18d5">EnumTypeDefs</a>
</td>
<td align="left" width="63%">
Enumerates TypeDef tokens representing all types within the current scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d77548d-dfba-4be1-b19d-41b21ab3a112">EnumTypeRefs</a>
</td>
<td align="left" width="63%">
Enumerates TypeRef tokens defined in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81b3b750-b9bd-42f1-b49d-134a10493ae5">EnumTypeSpecs</a>
</td>
<td align="left" width="63%">
Enumerates TypeSpec tokens defined in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c10a1af-93a5-44d0-818f-f307f5f81075">EnumUnresolvedMethods</a>
</td>
<td align="left" width="63%">
Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/646f6e8a-4c78-493c-90e2-2114bce82c46">EnumUserStrings</a>
</td>
<td align="left" width="63%">
Enumerates String tokens representing hard-coded strings in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beb32bb3-06e3-4817-90f0-0745756e1955">FindMemberRef</a>
</td>
<td align="left" width="63%">
Gets a pointer to the MemberRef token for the member reference that is enclosed by the specified Type and that has the specified name and metadata signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd4dd7d9-dfdf-4095-881b-c730ebfb083c">FindTypeDefByName</a>
</td>
<td align="left" width="63%">
Gets a pointer to the TypeDef metadata token for the Type with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec89d7c0-b607-4885-b819-3eb8022ad46d">FindTypeRef</a>
</td>
<td align="left" width="63%">
Gets a pointer to the TypeRef token for the Type reference that is in the specified scope and that has the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2771a90-4ac3-4c5a-869a-e18d1a4c6b3e">GetCustomAttributeByName</a>
</td>
<td align="left" width="63%">
Gets the custom attribute, given its name and owner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccb8891c-ceef-4897-9ec4-b3008a7d5264">GetCustomAttributeProps</a>
</td>
<td align="left" width="63%">
Gets the value of the custom attribute, given its metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a176ce92-761f-48fd-b9e8-01990176df27">GetFieldMarshal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the native, unmanaged type of the field represented by the specified field metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c935c4c-a7ac-49b9-af26-25f240ef78f2">GetFieldProps</a>
</td>
<td align="left" width="63%">
Gets metadata associated with the field referenced by the specified FieldDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff91bb07-8e3a-49f1-9cd6-1c3e18a3c242">GetInterfaceImplProps</a>
</td>
<td align="left" width="63%">
Gets a pointer to the metadata tokens for the Type that implements the specified method, and for the interface that declares that method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b278947f-4e84-4438-bb93-11bfd2d56be3">GetMemberProps</a>
</td>
<td align="left" width="63%">
Gets metadata information, including the name, binary signature, and relative virtual address, of the Type member referenced by the specified metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a82baa9a-0102-4d30-945d-34ec2514e0a6">GetMemberRefProps</a>
</td>
<td align="left" width="63%">
Gets metadata associated with the member referenced by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/973f2a8c-025d-4d27-ac99-56902b1132dd">GetMethodProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the method referenced by the specified MethodDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4133bf8-4ae4-43ad-8d07-4f7805e9ef2c">GetMethodSemantics</a>
</td>
<td align="left" width="63%">
Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ad7248d-7266-4a14-b499-05bda7f60e01">GetModuleFromScope</a>
</td>
<td align="left" width="63%">
Gets a metadata token for the module referenced in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f14fe81-d585-4167-8817-0c7d000413de">GetModuleRefProps</a>
</td>
<td align="left" width="63%">
Gets the name of the module referenced by the specified metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/933d502a-c752-45ae-b51f-8c0a876856bc">GetNameFromToken</a>
</td>
<td align="left" width="63%">
Gets the UTF-8 name of the object referenced by the specified metadata token. This method is obsolete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90e09d3d-c77e-44c3-b4d0-6b2aee995b1e">GetNativeCallConvFromSig</a>
</td>
<td align="left" width="63%">
Gets the native calling convention for the method that is represented by the specified signature pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5633d226-8f02-4527-b435-b75b1e1d5064">GetNestedClassProps</a>
</td>
<td align="left" width="63%">
Gets the TypeDef token for the parent Type of the specified nested type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/118a5ab3-b7db-4e0c-bf45-ab7e2e0e4f03">GetParamForMethodIndex</a>
</td>
<td align="left" width="63%">
Gets the token that represents a specified parameter of the method represented by the specified MethodDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76de324f-f371-4fac-ab0a-b7f359dd3abd">GetParamProps</a>
</td>
<td align="left" width="63%">
Gets metadata values for the parameter referenced by the specified ParamDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db10bdb6-3150-4eb9-872a-3f56089812fa">GetPermissionSetProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the System.Security.PermissionSet represented by the specified Permission token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf83785d-ba4f-4a11-84ee-92d010c8a1fc">GetPinvokeMap</a>
</td>
<td align="left" width="63%">
Gets a ModuleRef token to represent the target assembly of a PInvoke call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/125f7891-0ffe-48f9-a9de-4b4d2f50fc25">GetRVA</a>
</td>
<td align="left" width="63%">
Gets the relative virtual address (RVA) and the implementation flags of the method or field represented by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7c7cc92-fa0e-426d-b26d-d8f87bffad7d">GetScopeProps</a>
</td>
<td align="left" width="63%">
Gets the name and optionally the version identifier of the assembly or module in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/babd95ef-7786-47da-b5f6-c1fef93a4504">GetSigFromToken</a>
</td>
<td align="left" width="63%">
Gets the binary metadata signature associated with the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/447937af-5edb-4e5e-89a1-13d1a733b3f7">GetTypeDefProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the Type referenced by the specified TypeRef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/714d1adf-df8d-4f6b-8bcd-8dd9461c102a">GetTypeRefProps</a>
</td>
<td align="left" width="63%">
Returns metadata information for the Type represented by the specified TypeDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e03b6c5f-c68a-44a9-a203-8ed00293b582">GetTypeSpecFromToken</a>
</td>
<td align="left" width="63%">
Gets the binary metadata signature of the type specification represented by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c809d878-7c9a-4759-83c8-31cb0a72ee9d">GetUserString</a>
</td>
<td align="left" width="63%">
Gets the literal string represented by the specified metadata token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01558f0f-11ca-4c17-8f55-b0fc78492813">IsGlobal</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the field, method, or type represented by the specified metadata token has global scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9829a600-38fb-48ac-a486-abb56d17afdf">IsValidToken</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the specified token holds a valid reference to a code object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74168393-e2ec-44bb-9fae-2c76ad40a3f8">ResetEnum</a>
</td>
<td align="left" width="63%">
Resets the specified enumerator to the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d19d47c7-bf06-4daa-bda6-8aca6939a543">ResolveTypeRef</a>
</td>
<td align="left" width="63%">
Resolves a Type reference represented by the specified TypeRef token.

</td>
</tr>
</table> 

