---
UID: NF:certenc.ICertEncodeDateArray.SetValue
title: ICertEncodeDateArray::SetValue (certenc.h)
description: Sets a DATE value at the specified index of the DATE array.
old-location: security\icertencodedatearray_setvalue.htm
tech.root: SecCrypto
ms.assetid: e05a7aa1-81ad-4564-a6a5-65b8ac816598
ms.date: 12/05/2018
ms.keywords: CCertEncodeDateArray object [Security],SetValue method, ICertEncodeDateArray interface [Security],SetValue method, ICertEncodeDateArray.SetValue, ICertEncodeDateArray::SetValue, SetValue, SetValue method [Security], SetValue method [Security],CCertEncodeDateArray object, SetValue method [Security],ICertEncodeDateArray interface, _certsrv_icertencodedatearray_setvalue, certenc/ICertEncodeDateArray::SetValue, security.icertencodedatearray_setvalue
ms.topic: method
f1_keywords:
- certenc/ICertEncodeDateArray.SetValue
dev_langs:
- c++
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
- ICertEncodeDateArray.SetValue
- CCertEncodeDateArray.SetValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertEncodeDateArray::SetValue


## -description


The <b>SetValue</b> method sets a <b>DATE</b> value at the specified index of the <b>DATE</b> array.

 You must call 
the <a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-reset">ICertEncodeDateArray::Reset</a> method before calling <b>SetValue</b> for the first time.


## -parameters




### -param Index [in]

The zero-based index that specifies the index of the date element to set. 


### -param Value [in]

Specifies the <b>DATE</b> value to set.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nn-certenc-icertencodedatearray">ICertEncodeDateArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-getvalue">ICertEncodeDateArray::GetValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-reset">ICertEncodeDateArray::Reset</a>
 

 

