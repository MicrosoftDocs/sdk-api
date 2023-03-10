---
UID: NF:certview.IEnumCERTVIEWEXTENSION.GetValue
title: IEnumCERTVIEWEXTENSION::GetValue (certview.h)
description: Retrieves the value of the current extension in the extension-enumeration sequence.
helpviewer_keywords: ["CV_OUT_BASE64","CV_OUT_BASE64HEADER","CV_OUT_BASE64REQUESTHEADER","CV_OUT_BINARY","CV_OUT_HEX","CV_OUT_HEXADDR","CV_OUT_HEXASCII","CV_OUT_HEXASCIIADDR","GetValue","GetValue method [Security]","GetValue method [Security]","IEnumCERTVIEWEXTENSION interface","IEnumCERTVIEWEXTENSION interface [Security]","GetValue method","IEnumCERTVIEWEXTENSION.GetValue","IEnumCERTVIEWEXTENSION::GetValue","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","_certsrv_ienumcertviewextension_getvalue","certview/IEnumCERTVIEWEXTENSION::GetValue","security.ienumcertviewextension_getvalue"]
old-location: security\ienumcertviewextension_getvalue.htm
tech.root: security
ms.assetid: 7a81b096-36ba-416a-ad15-5bf1c4d512dd
ms.date: 12/05/2018
ms.keywords: CV_OUT_BASE64, CV_OUT_BASE64HEADER, CV_OUT_BASE64REQUESTHEADER, CV_OUT_BINARY, CV_OUT_HEX, CV_OUT_HEXADDR, CV_OUT_HEXASCII, CV_OUT_HEXASCIIADDR, GetValue, GetValue method [Security], GetValue method [Security],IEnumCERTVIEWEXTENSION interface, IEnumCERTVIEWEXTENSION interface [Security],GetValue method, IEnumCERTVIEWEXTENSION.GetValue, IEnumCERTVIEWEXTENSION::GetValue, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, _certsrv_ienumcertviewextension_getvalue, certview/IEnumCERTVIEWEXTENSION::GetValue, security.ienumcertviewextension_getvalue
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
 - IEnumCERTVIEWEXTENSION::GetValue
 - certview/IEnumCERTVIEWEXTENSION::GetValue
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
 - IEnumCERTVIEWEXTENSION.GetValue
 - IEnumCERTVIEWEXTENSION.GetValue
---

# IEnumCERTVIEWEXTENSION::GetValue


## -description

The <b>GetValue</b> method retrieves the value of the current extension in the extension-enumeration sequence.

## -parameters

### -param Type [in]

Data type for the returned data. This parameter can be used to specify that the extension data be decoded before being returned. If PROPTYPE_BINARY is specified, the data is not decoded but instead returned in its raw format. 




               

 Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
The extension value is retrieved as is and is ASN.1 encoded if necessary.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
Extension value is returned as            a date/time.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_LONG"></a><a id="proptype_long"></a><dl>
<dt><b>PROPTYPE_LONG</b></dt>
</dl>
</td>
<td width="60%">
Extension value is returned as            a signed long.
                     

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
The extension value is ASN.1 encoded as an IA5 string.

</td>
</tr>
</table>

### -param Flags [in]

Flag  that denotes the output format for the returned data. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64"></a><a id="cv_out_base64"></a><dl>
<dt><b>CV_OUT_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 without BEGIN/END

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64HEADER"></a><a id="cv_out_base64header"></a><dl>
<dt><b>CV_OUT_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN CERTIFICATE and END CERTIFICATE

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64REQUESTHEADER"></a><a id="cv_out_base64requestheader"></a><dl>
<dt><b>CV_OUT_BASE64REQUESTHEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN NEW CERTIFICATE REQUEST and END NEW CERTIFICATE REQUEST

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BINARY"></a><a id="cv_out_binary"></a><dl>
<dt><b>CV_OUT_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEX"></a><a id="cv_out_hex"></a><dl>
<dt><b>CV_OUT_HEX</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXADDR"></a><a id="cv_out_hexaddr"></a><dl>
<dt><b>CV_OUT_HEXADDR</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with address/offset

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXASCII"></a><a id="cv_out_hexascii"></a><dl>
<dt><b>CV_OUT_HEXASCII</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with ASCII

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXASCIIADDR"></a><a id="cv_out_hexasciiaddr"></a><dl>
<dt><b>CV_OUT_HEXASCIIADDR</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with ASCII and address/offset

</td>
</tr>
</table>

### -param pvarValue [out]

A pointer to a value of <b>VARIANT</b> type that contains the data for the currently referenced extension. This method fails if the   <i>pvarValue</i> parameter is <b>NULL</b>. Upon successful completion of this function, <i>pvarValue</i> contains the extension data currently referenced by the extension-enumeration sequence. The caller is responsible for calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> when done with the data in <i>pvarValue</i>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>Variant</b> that represents the data in the extension.

## -remarks

This method is used to retrieve the data in the extension currently being referenced by the 
extension-enumeration sequence.

If the extension-enumeration sequence is not referencing a valid extension, <b>GetValue</b> fails.  Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-reset">IEnumCERTVIEWEXTENSION::Reset</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">IEnumCERTVIEWEXTENSION::Next</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-skip">IEnumCERTVIEWEXTENSION::Skip</a>: Skips a specified number of extensions.</li>
</ul>
This method fails if the extension-enumeration sequence was obtained by a call to the  
<a href="/windows/desktop/api/certview/nf-certview-icertview-enumcertviewcolumn">ICertView::EnumCertViewColumn</a> method because  enumeration sequences obtained by that method contain only schema information.


#### Examples


```cpp
VARIANT     var;
LONG        Index;
HRESULT     hr;
SYSTEMTIME  systime;

VariantInit(&var);

// Enumerate each extension
// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
while (S_OK == pEnumExt->Next(&Index))
{
    hr = pEnumExt->GetValue(PROPTYPE_BINARY, CV_OUT_HEX, &var);
    if (FAILED(hr))
    {
        printf("Failed GetValue - %x\n", hr);
        break;
    }
    switch(var.vt)
    {
        case VT_EMPTY:
            printf("VT_EMPTY\n");
            break;
        case VT_BSTR:
            printf("BSTR:%ws\n", var.bstrVal);
            break;
        case VT_DATE:
            VariantTimeToSystemTime(var.date, &systime);
            printf("%d.%d.%d %02d:%02d:%02d\n",
                   systime.wMonth,
                   systime.wDay,
                   systime.wYear,
                   systime.wHour,
                   systime.wMinute,
                   systime.wSecond );
            break;
        case VT_I2:
            printf("%d\n", var.iVal);
            break;
        case VT_I4:
            printf("%d\n", var.lVal);
            break;
        default:
            printf("type is:%i\n", var.vt);
            break;
    }
}
// Free resources.
VariantClear( &var );
```

## -see-also

<a href="/windows/desktop/api/certview/nf-certview-icertview-enumcertviewcolumn">ICertView::EnumCertViewColumn</a>



<b>IEnumCERTVIEWEXTENSION</b>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">IEnumCERTVIEWEXTENSION::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-reset">IEnumCERTVIEWEXTENSION::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-skip">IEnumCERTVIEWEXTENSION::Skip</a>