---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DRMVerify function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]
<p class="CCE_Message">[The <b>DRMVerify</b> function is no longer supported and returns E_NOTIMPL.]

For Rights Management Services 1.0, the <b>DRMVerify</b> function verifies data signed with <a href="https://msdn.microsoft.com/f0975845-d609-4f7a-a663-6481334c983d">DRMAttest</a>.


## -parameters




### -param wszData [in]

The data to verify (original data).


### -param pcAttestedData

TBD


### -param wszAttestedData [out]

The signed data.


### -param peType [out]

Whether full environment information,  or just a hash of the environment, is included.


### -param pcPrincipal

TBD


### -param wszPrincipal

TBD


### -param pcManifest

TBD


### -param wszManifest

TBD




#### - pcManifestChain [in, out]

Size, in characters, of the manifest used to sign the data, plus one for a terminating null character. For information about making a manifest, see <a href="https://msdn.microsoft.com/dc5e2d57-bacc-43cc-8f97-a2962812fa6c">Creating an Application Manifest</a>.


#### - pcPrincipalChain [in, out]

Size, in characters, of the <i>wszPrincipalCredentials</i> parameter, plus one for a terminating null character.


#### - pcStrLenAttestedData [in, out]

Length, in characters, of the data to verify, plus one for a terminating null character.


#### - wszManifestChain [out]

The manifest used to sign, as a null-terminated string.


#### - wszPrincipalChain [out]

Certificate chain of the principal attesting the data. This chain is needed to create the principal used to verify the data.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 

