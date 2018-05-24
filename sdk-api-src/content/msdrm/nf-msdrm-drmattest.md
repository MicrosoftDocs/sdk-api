---
UID: NF:msdrm.DRMAttest
title: DRMAttest function
author: windows-driver-content
description: The DRMAttest function is no longer supported and returns E_NOTIMPL.
old-location: rm\drmattest.htm
old-project: AdRms_Sdk
ms.assetid: f0975845-d609-4f7a-a663-6481334c983d
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRMAttest, DRMAttest function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMAttest, rm.drmattest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMAttest
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DRMAttest function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]
<p class="CCE_Message">[The <b>DRMAttest</b> function is no longer supported and returns E_NOTIMPL.]

For Rights Management Services 1.0, the <b>DRMAttest</b> function signs arbitrary data.


## -parameters




### -param hEnablingPrincipal [in]

A handle to an enabling principal object created by using <a href="https://msdn.microsoft.com/92858a46-cef5-4d25-9f3c-cbb343743565">DRMCreateEnablingPrincipal</a>.


### -param wszData [in]

The data to encode.


### -param eType [in]

An enumeration that determines whether to include full environment data or only a hash.


### -param pcAttestedBlob

TBD


### -param wszAttestedBlob [out]

The signed data.


#### - pcStrLen [in, out]

Length, in characters, of the string being returned, plus one for a terminating null character.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function can be used with challenge/response protocols by including the challenge in the data buffer. An output string may contain the principal's certificates, in addition to the signature.

The data is concatenated with the manifest used to initialize the RM environment. A manifest is a signed XrML blob that includes information to authenticate the program and all required DLLs, as well as a list of any prohibited DLLs. The manifest used is the one loaded when the RM environment was initialized. For information about making a manifest, see <a href="https://msdn.microsoft.com/dc5e2d57-bacc-43cc-8f97-a2962812fa6c">Creating an Application Manifest</a>.

To return a value, first call this function with <b>NULL</b> passed into the <i>wszAttestedBlob</i> parameter. The value returned in <i>pcStrLen</i> will indicate the size of the variable the application must create to hold the encoded signature. All buffer allocation and destruction are the responsibility of the caller.

Data signed by using <b>DRMAttest</b> can be verified by using <a href="https://msdn.microsoft.com/aebf46e7-9de2-40e7-a748-0621a61ccb6a">DRMVerify</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 

