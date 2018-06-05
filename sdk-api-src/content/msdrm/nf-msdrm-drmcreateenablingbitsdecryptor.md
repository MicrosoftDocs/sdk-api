---
UID: NF:msdrm.DRMCreateEnablingBitsDecryptor
title: DRMCreateEnablingBitsDecryptor function
author: windows-sdk-content
description: Creates a decryption object that is used to decrypt content data.
old-location: rm\drmcreateenablingbitsdecryptor.htm
old-project: AdRms_Sdk
ms.assetid: 133582e2-6396-476f-a28b-37ed0257fb79
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMCreateEnablingBitsDecryptor, DRMCreateEnablingBitsDecryptor function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateEnablingBitsDecryptor, rm.drmcreateenablingbitsdecryptor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMCreateEnablingBitsDecryptor
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateEnablingBitsDecryptor function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateEnablingBitsDecryptor</b> function creates a decryption object that is used to decrypt content data.


## -parameters




### -param hBoundLicense [in]

A handle to a bound license object created by using <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>.


### -param wszRight [in, optional]

An optional null-terminated string that contains the right to exercise. A decrypting object can be bound to only one right at a time.


### -param hAuxLib [in]

Reserved for future use. This parameter must be <b>NULL</b>.


### -param wszAuxPlug [in, optional]

Reserved for future use. This parameter must be <b>NULL</b>.


### -param phDecryptor [out]

A pointer to the decrypting object.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



A consuming application performs the following steps to decrypt content previously encrypted by a publishing application.<ol>
<li>Retrieve an end-user license. Call <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> to retrieve the license if it already exists in the store. If function succeeds, go to step 2. If the license is not in the store, call <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a> followed by <b>DRMEnumerateLicense</b>.</li>
<li>Call <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a> to create a license that binds to one or more rights in the end-user license. The bound license includes a symmetric key that can be used for decryption.</li>
<li>Call <b>DRMCreateEnablingBitsDecryptor</b> to create an decrypting object associated with the bound right and content key.</li>
<li>Call <a href="https://msdn.microsoft.com/8e0cb353-4670-4cf7-bcd8-81ebd0adfe32">DRMDecrypt</a> to use the content key to decrypt the content.</li>
</ol>


Call the <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a> function to close the decrypting object handle when you are finished with it. Both the decrypting object handle and the bound license handle must remain open until decryption is complete.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/f3875ddd-293e-4abb-b468-a6754bc361a0">DRMCreateEnablingBitsEncryptor</a>



<a href="https://msdn.microsoft.com/768767a0-b76c-4a9a-a4b1-22dd1923c667">Decrypting Content</a>
 

 

