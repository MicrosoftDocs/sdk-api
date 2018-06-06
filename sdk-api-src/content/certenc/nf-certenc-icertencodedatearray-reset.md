---
UID: NF:certenc.ICertEncodeDateArray.Reset
title: ICertEncodeDateArray::Reset
author: windows-sdk-content
description: Specifies the size of DATE array in this object.
old-location: security\icertencodedatearray_reset.htm
old-project: SecCrypto
ms.assetid: f09087aa-ae10-4a59-9b59-5f8b72254ce6
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CCertEncodeDateArray object [Security],Reset method, ICertEncodeDateArray interface [Security],Reset method, ICertEncodeDateArray.Reset, ICertEncodeDateArray::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeDateArray object, Reset method [Security],ICertEncodeDateArray interface, _certsrv_icertencodedatearray_reset, certenc/ICertEncodeDateArray::Reset, security.icertencodedatearray_reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: X509EnrollmentAuthFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeDateArray.Reset
 - CCertEncodeDateArray.Reset
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeDateArray::Reset


## -description


The <b>Reset</b> method specifies the size of <b>DATE</b> array in this object. The values of all the elements in the array are set to zero. You must call this method before calling the <a href="https://msdn.microsoft.com/e05a7aa1-81ad-4564-a6a5-65b8ac816598">ICertEncodeDateArray::SetValue</a> method for the first time.


## -parameters




### -param Count [in]

Specifies the number of elements in the <b>DATE</b> array.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/9973c49a-d886-4cc4-b75e-7ff46f56d51c">ICertEncodeDateArray</a>



<a href="https://msdn.microsoft.com/e05a7aa1-81ad-4564-a6a5-65b8ac816598">ICertEncodeDateArray::SetValue</a>
 

 

