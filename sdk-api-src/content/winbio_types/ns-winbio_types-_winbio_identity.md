---
UID: NS:winbio_types._WINBIO_IDENTITY
title: "_WINBIO_IDENTITY"
author: windows-driver-content
description: Contains an identifying value associated with a biometric template.
old-location: secbiomet\winbio_identity.htm
old-project: SecBioMet
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_IDENTITY, WINBIO_IDENTITY, WINBIO_IDENTITY structure [Windows Biometric Framework API], WINBIO_ID_TYPE_GUID, WINBIO_ID_TYPE_NULL, WINBIO_ID_TYPE_SID, WINBIO_ID_TYPE_WILDCARD, _WINBIO_IDENTITY, secbiomet.winbio_identity, winbio_types/WINBIO_IDENTITY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_types.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_IDENTITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_IDENTITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_IDENTITY structure


## -description


The <b>WINBIO_IDENTITY</b> structure contains an  identifying value associated with a biometric template.


## -struct-fields




### -field Value

A union that can contain one of the following values:



#### Null

Contains 1 if the <b>Type</b> member is <b>WINBIO_ID_TYPE_NULL</b>.



#### Wildcard

Contains 1 if the <b>Type</b> member is <b>WINBIO_ID_TYPE_WILDCARD</b>.



#### TemplateGuid

Contains a 128-bit GUID value that identifies the template if the <b>Type</b> member is <b>WINBIO_ID_TYPE_GUID</b>.


### -field Value.AccountSid

A structure that contains an account SID if the <b>Type</b> member is <b>WINBIO_ID_TYPE_SID</b>.


### -field Value.AccountSid.Size

The number of characters in the SID.


### -field Value.AccountSid.Data

An array of unsigned characters that contain the SID. The current maximum size of the array is 68 characters.


### -field Type

Specifies the format of the identity information contained in this structure. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_ID_TYPE_NULL"></a><a id="winbio_id_type_null"></a><dl>
<dt><b>WINBIO_ID_TYPE_NULL</b></dt>
</dl>
</td>
<td width="60%">
The template has no associated ID.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_ID_TYPE_WILDCARD"></a><a id="winbio_id_type_wildcard"></a><dl>
<dt><b>WINBIO_ID_TYPE_WILDCARD</b></dt>
</dl>
</td>
<td width="60%">
The structure matches all template identities.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_ID_TYPE_GUID"></a><a id="winbio_id_type_guid"></a><dl>
<dt><b>WINBIO_ID_TYPE_GUID</b></dt>
</dl>
</td>
<td width="60%">
The structure contains a GUID associated with the template.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_ID_TYPE_SID"></a><a id="winbio_id_type_sid"></a><dl>
<dt><b>WINBIO_ID_TYPE_SID</b></dt>
</dl>
</td>
<td width="60%">
The structure contains the account SID associated with the template.

</td>
</tr>
</table>
 


## -remarks



This structure is used in the following functions:<ul>
<li>
<a href="https://msdn.microsoft.com/aad22c42-d306-42b5-8415-0b561c8bcecf">WinBioDeleteTemplate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ed9242e5-fee7-46ca-b42c-cda1b5dcdc78">WinBioEnrollCommit</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bd5fd36a-ed90-4dd0-8a84-0412544493dd">WinBioEnumEnrollments</a>
</li>
<li>
<a href="https://msdn.microsoft.com/738b7efb-c796-4f64-95e3-feaaa50ac673">WinBioGetCredentialState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aaa9b4cd-81d4-4fee-a40a-5563997c42e8">WinBioIdentify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/56a5d510-f2cb-457b-884a-ad08ea21ce01">WinBioRemoveCredential</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7266ca33-d3f9-421f-8265-e23a3ec3a77e">WinBioVerify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ea03163-062a-4abf-837a-b12b03ada375">WinBioVerifyWithCallback</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>
 

 

