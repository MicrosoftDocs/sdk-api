---
UID: NF:certview.IEnumCERTVIEWEXTENSION.Next
title: IEnumCERTVIEWEXTENSION::Next (certview.h)
description: Moves to the next extension in the extension-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWEXTENSION interface [Security]","Next method","IEnumCERTVIEWEXTENSION object [Security]","Next method","IEnumCERTVIEWEXTENSION.Next","IEnumCERTVIEWEXTENSION::Next","Next","Next method [Security]","Next method [Security]","IEnumCERTVIEWEXTENSION interface","Next method [Security]","IEnumCERTVIEWEXTENSION object","_certsrv_ienumcertviewextension_next","certview/IEnumCERTVIEWEXTENSION::Next","security.ienumcertviewextension_next"]
old-location: security\ienumcertviewextension_next.htm
tech.root: security
ms.assetid: 658daf9d-0f61-4c93-9688-a7c74464ca89
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWEXTENSION interface [Security],Next method, IEnumCERTVIEWEXTENSION object [Security],Next method, IEnumCERTVIEWEXTENSION.Next, IEnumCERTVIEWEXTENSION::Next, Next, Next method [Security], Next method [Security],IEnumCERTVIEWEXTENSION interface, Next method [Security],IEnumCERTVIEWEXTENSION object, _certsrv_ienumcertviewextension_next, certview/IEnumCERTVIEWEXTENSION::Next, security.ienumcertviewextension_next
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumCERTVIEWEXTENSION::Next
 - certview/IEnumCERTVIEWEXTENSION::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IEnumCERTVIEWEXTENSION.Next
 - IEnumCERTVIEWEXTENSION.Next
---

# IEnumCERTVIEWEXTENSION::Next


## -description

The <b>Next</b> method moves to the next extension in the extension-enumeration sequence.

## -parameters

### -param pIndex [out]

A pointer to a variable that contains the index value of the next extension being referenced. If there are no more extensions to enumerate, this variable will be set to –1. This method fails if <i>pIndex</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the next extension is now being referenced. If there are no more extensions, S_FALSE is returned, and the  <i>pIndex</i> parameter is set to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the index value of the extension that is now referenced by the extension-enumeration sequence. If there are no more extensions to enumerate, the return value is –1.

## -remarks

Upon successful completion of this method, the extension name, flags, and value can be accessed through 
the following methods:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getname">IEnumCERTVIEWEXTENSION::GetName</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getflags">IEnumCERTVIEWEXTENSION::GetFlags</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getvalue">IEnumCERTVIEWEXTENSION::GetValue</a>
</li>
</ul>

#### Examples


```cpp
LONG  Index;
LONG  nCount;

// determine the number of extensions
nCount = 0;
// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
while (S_OK == pEnumExt->Next(&Index))
{
    nCount++;
}
printf("Number of extensions is %d\n", nCount);
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getflags">IEnumCERTVIEWEXTENSION::GetFlags</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getname">IEnumCERTVIEWEXTENSION::GetName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getvalue">IEnumCERTVIEWEXTENSION::GetValue</a>