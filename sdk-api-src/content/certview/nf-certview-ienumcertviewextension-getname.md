---
UID: NF:certview.IEnumCERTVIEWEXTENSION.GetName
title: IEnumCERTVIEWEXTENSION::GetName (certview.h)
description: Retrieves the name of the current extension in the extension-enumeration sequence.
helpviewer_keywords: ["CEnumCERTVIEWEXTENSION object [Security]","GetName method","GetName","GetName method [Security]","GetName method [Security]","CEnumCERTVIEWEXTENSION object","GetName method [Security]","IEnumCERTVIEWEXTENSION interface","IEnumCERTVIEWEXTENSION interface [Security]","GetName method","IEnumCERTVIEWEXTENSION.GetName","IEnumCERTVIEWEXTENSION::GetName","_certsrv_ienumcertviewextension_getname","certview/IEnumCERTVIEWEXTENSION::GetName","security.ienumcertviewextension_getname"]
old-location: security\ienumcertviewextension_getname.htm
tech.root: security
ms.assetid: 7c56708c-ae25-46f5-94f3-d58eea8d08d4
ms.date: 12/05/2018
ms.keywords: CEnumCERTVIEWEXTENSION object [Security],GetName method, GetName, GetName method [Security], GetName method [Security],CEnumCERTVIEWEXTENSION object, GetName method [Security],IEnumCERTVIEWEXTENSION interface, IEnumCERTVIEWEXTENSION interface [Security],GetName method, IEnumCERTVIEWEXTENSION.GetName, IEnumCERTVIEWEXTENSION::GetName, _certsrv_ienumcertviewextension_getname, certview/IEnumCERTVIEWEXTENSION::GetName, security.ienumcertviewextension_getname
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
 - IEnumCERTVIEWEXTENSION::GetName
 - certview/IEnumCERTVIEWEXTENSION::GetName
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
 - IEnumCERTVIEWEXTENSION.GetName
 - CEnumCERTVIEWEXTENSION.GetName
---

# IEnumCERTVIEWEXTENSION::GetName


## -description

The <b>GetName</b> method retrieves the name of the current extension in the extension-enumeration sequence.

 The returned extension name is an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) string, as in L"2.5.29.31".

## -parameters

### -param pstrOut [out]

A pointer to a value of <b>BSTR</b> type that contains the name of the extension.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and tat the <i>pstrOut</i> parameter is set to the name of the extension.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrOut</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that contains the name of the extension.

## -remarks

This function is used to retrieve the name of the extension currently referenced by the 
extension-enumeration sequence.

If the extension-enumeration sequence is not referencing a valid extension, <b>GetName</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-reset">IEnumCERTVIEWEXTENSION::Reset</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">IEnumCERTVIEWEXTENSION::Next</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-skip">IEnumCERTVIEWEXTENSION::Skip</a>: Skips a specified number of extensions.</li>
</ul>

#### Examples


```cpp
BSTR  bstrExtName = NULL;

// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
hr = pEnumExt->GetName(&bstrExtName);
if (S_OK == hr)
    printf("Extension name is: %ws\n", bstrExtName);
else
    printf("GetName failed: %x\n", hr);

// free memory when done
if (NULL != bstrExtName)
    SysFreeString(bstrExtName);
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewextension">IEnumCERTVIEWEXTENSION</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getflags">IEnumCERTVIEWEXTENSION::GetFlags</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getvalue">IEnumCERTVIEWEXTENSION::GetValue</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">IEnumCERTVIEWEXTENSION::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-reset">IEnumCERTVIEWEXTENSION::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-skip">IEnumCERTVIEWEXTENSION::Skip</a>