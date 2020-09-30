---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.Next
title: IEnumCERTVIEWATTRIBUTE::Next (certview.h)
description: Moves to the next attribute in the attribute-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWATTRIBUTE interface [Security]","Next method","IEnumCERTVIEWATTRIBUTE.Next","IEnumCERTVIEWATTRIBUTE::Next","Next","Next method [Security]","Next method [Security]","IEnumCERTVIEWATTRIBUTE interface","_certsrv_ienumcertviewattribute_next","certview/IEnumCERTVIEWATTRIBUTE::Next","security.ienumcertviewattribute_next"]
old-location: security\ienumcertviewattribute_next.htm
tech.root: security
ms.assetid: 2903ccda-e06d-4690-accf-79bc73d8569f
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWATTRIBUTE interface [Security],Next method, IEnumCERTVIEWATTRIBUTE.Next, IEnumCERTVIEWATTRIBUTE::Next, Next, Next method [Security], Next method [Security],IEnumCERTVIEWATTRIBUTE interface, _certsrv_ienumcertviewattribute_next, certview/IEnumCERTVIEWATTRIBUTE::Next, security.ienumcertviewattribute_next
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
 - IEnumCERTVIEWATTRIBUTE::Next
 - certview/IEnumCERTVIEWATTRIBUTE::Next
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
 - IEnumCERTVIEWATTRIBUTE.Next
 - IEnumCERTVIEWATTRIBUTE.Next
---

# IEnumCERTVIEWATTRIBUTE::Next


## -description

The <b>Next</b> method moves to the next  attribute in the attribute-enumeration sequence.

## -parameters

### -param pIndex [out]

A pointer to a variable that contains the index value of the next <a href="/windows/desktop/SecGloss/a-gly">attribute</a> being referenced. If there are no more attributes to enumerate, this variable is set to –1. This method fails if <i>pIndex</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and  the next attribute is now being referenced by the attribute-enumeration sequence.  If there are no more attributes, the method returns S_FALSE, and <i>pIndex</i> is set to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the index value of the attribute that is now referenced by the attribute-enumeration sequence. If there are no more attributes to enumerate, the return value is –1.

## -remarks

Upon successful completion of this method, the attribute name and value can be accessed through the 
following methods:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getname">IEnumCERTVIEWATTRIBUTE::GetName</a>
</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getvalue">IEnumCERTVIEWATTRIBUTE::GetValue</a>
</li>
</ul>

#### Examples


```cpp
LONG       Index;
HRESULT    hr;
BSTR       bstrAttribName = NULL;

// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
while (S_OK == pEnumAttr->Next(&Index))
{
    // retrieve the attribute name
    hr = pEnumAttr->GetName(&bstrAttribName);
    if (FAILED(hr))
        printf("Failed GetName -  %x\n", hr );
    else
        printf("Attribute name: %ws\n", bstrAttribName);
}

// Free resources.
if (NULL != bstrAttribName)
    SysFreeString(bstrAttribName);
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getname">IEnumCERTVIEWATTRIBUTE::GetName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getvalue">IEnumCERTVIEWATTRIBUTE::GetValue</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-reset">IEnumCERTVIEWATTRIBUTE::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-skip">IEnumCERTVIEWATTRIBUTE::Skip</a>