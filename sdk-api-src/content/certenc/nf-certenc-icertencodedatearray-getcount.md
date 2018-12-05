---
UID: NF:certenc.ICertEncodeDateArray.GetCount
title: ICertEncodeDateArray::GetCount
author: windows-sdk-content
description: Returns the number of DATE values in the object's DATE array.
old-location: security\icertencodedatearray_getcount.htm
tech.root: seccrypto
ms.assetid: 25c61f42-b190-44c3-b2ba-57861bdfbce3
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: CCertEncodeDateArray object [Security],GetCount method, GetCount, GetCount method [Security], GetCount method [Security],CCertEncodeDateArray object, GetCount method [Security],ICertEncodeDateArray interface, ICertEncodeDateArray interface [Security],GetCount method, ICertEncodeDateArray.GetCount, ICertEncodeDateArray::GetCount, _certsrv_icertencodedatearray_getcount, certenc/ICertEncodeDateArray::GetCount, security.icertencodedatearray_getcount
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeDateArray.GetCount
 - CCertEncodeDateArray.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeDateArray::GetCount


## -description


The <b>GetCount</b> method returns the number of <b>DATE</b> values in the object's <b>DATE</b> array.


## -parameters




### -param pCount [out]

A pointer to a <b>LONG</b> that receives the number of <b>DATE</b> values contained in the <b>DATE</b> array.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of <b>DATE</b> values contained in the <b>DATE</b> array.




## -see-also




<a href="https://msdn.microsoft.com/9973c49a-d886-4cc4-b75e-7ff46f56d51c">ICertEncodeDateArray</a>



<a href="https://msdn.microsoft.com/db108b2a-c3ee-4ef8-be5c-74dc739dacee">ICertEncodeDateArray::GetValue</a>



<a href="https://msdn.microsoft.com/f09087aa-ae10-4a59-9b59-5f8b72254ce6">ICertEncodeDateArray::Reset</a>
 

 

