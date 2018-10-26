---
UID: NF:certview.IEnumCERTVIEWEXTENSION.Clone
title: IEnumCERTVIEWEXTENSION::Clone
author: windows-sdk-content
description: Creates a copy of the extension-enumeration sequence.
old-location: security\ienumcertviewextension_clone.htm
tech.root: seccrypto
ms.assetid: 2b8e19e4-459f-45f0-abb6-e1e0e115e0f5
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: Clone, Clone method [Security], Clone method [Security],IEnumCERTVIEWEXTENSION interface, IEnumCERTVIEWEXTENSION interface [Security],Clone method, IEnumCERTVIEWEXTENSION.Clone, IEnumCERTVIEWEXTENSION::Clone, _certsrv_ienumcertviewextension_clone, certview/IEnumCERTVIEWEXTENSION::Clone, security.ienumcertviewextension_clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certview.h
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
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IEnumCERTVIEWEXTENSION.Clone
 - IEnumCERTVIEWEXTENSION.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWEXTENSION::Clone


## -description


The <a href="https://msdn.microsoft.com/en-us/library/Aa386203(v=VS.85).aspx">Clone</a> method creates a copy of the extension-enumeration sequence.


## -parameters




### -param ppenum [out]

A pointer to a pointer of <a href="https://msdn.microsoft.com/en-us/library/Aa386203(v=VS.85).aspx">IEnumCERTVIEWEXTENSION</a> type. This method will fail if the <i>ppenum</i> parameter is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a cloned extension-enumeration sequence object.




## -remarks



The extension-enumeration sequence object is obtained by a call to the <a href="https://msdn.microsoft.com/en-us/library/Aa386242(v=VS.85).aspx">IEnumCERTVIEWROW::EnumCertViewExtension</a> method.


#### Examples


```cpp
IEnumCERTVIEWEXTENSION * pEnumExt2 = NULL;
HRESULT                  hr;

// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
hr = pEnumExt->Clone(&pEnumExt2);
if (S_OK != hr)
    printf("Unable to clone IEnumCERTVIEWEXTENSION\n");
else
{
    // use cloned object as needed
    //...
}
// done using cloned object, free memory
if (NULL != pEnumExt2)
    pEnumExt2->Release();
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386203(v=VS.85).aspx">IEnumCERTVIEWEXTENSION</a>
 

 

