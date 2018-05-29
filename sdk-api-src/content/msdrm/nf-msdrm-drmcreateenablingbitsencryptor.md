---
UID: NF:msdrm.DRMCreateEnablingBitsEncryptor
title: DRMCreateEnablingBitsEncryptor function
author: windows-sdk-content
description: Creates an AD RMS encrypting object that is used to encrypt content data.
old-location: rm\drmcreateenablingbitsencryptor.htm
old-project: AdRms_Sdk
ms.assetid: f3875ddd-293e-4abb-b468-a6754bc361a0
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMCreateEnablingBitsEncryptor, DRMCreateEnablingBitsEncryptor function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateEnablingBitsEncryptor, rm.drmcreateenablingbitsencryptor
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMCreateEnablingBitsEncryptor
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateEnablingBitsEncryptor function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateEnablingBitsEncryptor</b> function creates an AD RMS encrypting object that is used to encrypt content data.


## -parameters




### -param hBoundLicense [in]

A handle to a bound license, produced by <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>.


### -param wszRight [in, optional]

Optional null-terminated string containing a right. If you specify <b>NULL</b>, the AD RMS encrypting object binds to the first valid right in the license.


### -param hAuxLib [in]

Reserved for future use. This parameter must be <b>NULL</b>.


### -param wszAuxPlug [in, optional]

Reserved for future use. This parameter must be <b>NULL</b>.


### -param phEncryptor [out]

A pointer to the encrypting object.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Perform the following steps to encrypt content. For more information, see <a href="https://msdn.microsoft.com/30959fa0-54e0-43c7-9b76-8551ac06076f">Encrypting Content</a>.<ul>
<li>Acquire an end-user license. If the issuance license that you are using for this purpose was signed online, call <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a> followed by  <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a>. If the issuance license was signed offline, call <a href="https://msdn.microsoft.com/e657ac08-9635-40ac-8d9f-cc8ab9ed3a6c">DRMGetOwnerLicense</a> instead.</li>
<li>Call <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a> to create a license that binds to the EDIT or OWNER right in the end-user license. The bound license includes a symmetric key that can be used for encryption.</li>
<li>Call <b>DRMCreateEnablingBitsEncryptor</b> to create an encrypting object associated with the bound right and content key.</li>
<li>Call <a href="https://msdn.microsoft.com/1de19409-2b14-4ab0-9853-23ee5741a7ae">DRMEncrypt</a> to use the content key to encrypt the content.</li>
</ul>


Call the <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a> function to close the encrypting object handle when you are finished with it. Both the encrypting object handle and the bound license handle must remain open until encryption is complete.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/9948c2a4-cb42-42c1-bd22-33d39c039391">Creating and Using Issuance Licenses</a>



<a href="https://msdn.microsoft.com/133582e2-6396-476f-a28b-37ed0257fb79">DRMCreateEnablingBitsDecryptor</a>



<a href="https://msdn.microsoft.com/30959fa0-54e0-43c7-9b76-8551ac06076f">Encrypting Content</a>
 

 

