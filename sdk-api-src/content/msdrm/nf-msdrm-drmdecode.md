---
UID: NF:msdrm.DRMDecode
title: DRMDecode function
author: windows-driver-content
description: Decodes a string encoded with a common algorithm, such as base64.
old-location: rm\drmdecode.htm
old-project: AdRms_Sdk
ms.assetid: 380f9770-1d0c-453a-b737-04740608d7a7
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRMDecode, DRMDecode function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDecode, rm.drmdecode
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
-	DRMDecode
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMDecode function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDecode</b> function decodes a string encoded with a common algorithm, such as base64.


## -parameters




### -param wszAlgID [in]

The encoding algorithm name. Currently "base64" is the only valid value.


### -param wszEncodedString [in]

The encoded string.


### -param puDecodedDataLen [in]

The length of the decoded string, in characters, plus one for a null terminator.


### -param pbDecodedData [out]

Pointer to the decoded data.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Encoding is not the same as encrypting.

Buffer space for the decoded data must be allocated and freed by the caller. The size necessary for this buffer can be determined by calling this function with <b>NULL</b> in the <i>pbDecodedData</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/5fc0275c-098b-43a6-a52a-871321b0e4f3">DRMEncode</a>
 

 

