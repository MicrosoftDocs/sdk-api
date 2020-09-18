---
UID: NF:certview.IEnumCERTVIEWCOLUMN.GetValue
title: IEnumCERTVIEWCOLUMN::GetValue (certview.h)
description: Retrieves the data value contained in the current column in the column-enumeration sequence.
helpviewer_keywords: ["CV_OUT_BASE64","CV_OUT_BASE64HEADER","CV_OUT_BASE64REQUESTHEADER","CV_OUT_BASE64X509CRLHEADER","CV_OUT_BINARY","CV_OUT_HEX","CV_OUT_HEXADDR","CV_OUT_HEXASCII","CV_OUT_HEXASCIIADDR","GetValue","GetValue method [Security]","GetValue method [Security]","IEnumCERTVIEWCOLUMN interface","IEnumCERTVIEWCOLUMN interface [Security]","GetValue method","IEnumCERTVIEWCOLUMN.GetValue","IEnumCERTVIEWCOLUMN::GetValue","_certsrv_ienumcertviewcolumn_getvalue","certview/IEnumCERTVIEWCOLUMN::GetValue","security.ienumcertviewcolumn_getvalue"]
old-location: security\ienumcertviewcolumn_getvalue.htm
tech.root: security
ms.assetid: 5cc14bd1-7963-4b11-aef6-4ef3b0b7f6c1
ms.date: 12/05/2018
ms.keywords: CV_OUT_BASE64, CV_OUT_BASE64HEADER, CV_OUT_BASE64REQUESTHEADER, CV_OUT_BASE64X509CRLHEADER, CV_OUT_BINARY, CV_OUT_HEX, CV_OUT_HEXADDR, CV_OUT_HEXASCII, CV_OUT_HEXASCIIADDR, GetValue, GetValue method [Security], GetValue method [Security],IEnumCERTVIEWCOLUMN interface, IEnumCERTVIEWCOLUMN interface [Security],GetValue method, IEnumCERTVIEWCOLUMN.GetValue, IEnumCERTVIEWCOLUMN::GetValue, _certsrv_ienumcertviewcolumn_getvalue, certview/IEnumCERTVIEWCOLUMN::GetValue, security.ienumcertviewcolumn_getvalue
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
 - IEnumCERTVIEWCOLUMN::GetValue
 - certview/IEnumCERTVIEWCOLUMN::GetValue
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
 - IEnumCERTVIEWCOLUMN.GetValue
 - IEnumCERTVIEWCOLUMN.GetValue
---

# IEnumCERTVIEWCOLUMN::GetValue


## -description

The <b>GetValue</b> method retrieves the data value contained in the current column in the column-enumeration sequence.

## -parameters

### -param Flags [in]

An identifier that denotes the output format for the retrieved data. This parameter can be one of the following values.

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
<td width="40%"><a id="CV_OUT_BASE64X509CRLHEADER"></a><a id="cv_out_base64x509crlheader"></a><dl>
<dt><b>CV_OUT_BASE64X509CRLHEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN X509 CRL and END X509 CRL

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

A pointer to value of <b>VARIANT</b> type that contains the data column. This method fails if <i>pvarValue</i> is <b>NULL</b>. Upon successful completion of this method, <i>pvarValue</i> contains the data in the  column. The caller is responsible for calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> when done with this data.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>Variant</b> that represents the data in the column.

## -remarks

This method is used to retrieve the data in the column currently being referenced by the 
column-enumeration sequence.

If the column-enumeration sequence is not referencing a valid column, <b>GetValue</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-reset">IEnumCERTVIEWCOLUMN::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN::Next</a>: Moves to the next column in the enumeration sequence.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-skip">IEnumCERTVIEWCOLUMN::Skip</a>: Skips a specified number of columns.</li>
</ul>

#### Examples


```cpp
HRESULT     hr;
VARIANT     var;
SYSTEMTIME  systime;

VariantInit(&var);

// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
hr = pEnumCol->GetValue(CV_OUT_HEX, &var);
if ( FAILED (hr) )
{
    printf("Failed GetValue - %x\n", hr);
    goto error;
}
switch( var.vt )
{
    case VT_EMPTY:
        printf( "VT_EMPTY\n" );
        break;
    case VT_BSTR:
        printf("%ws\n", var.bstrVal );
        break;
    case VT_DATE:
        VariantTimeToSystemTime( var.date, &systime );
        printf("%d.%d.%d %02d:%02d:%02d\n",
               systime.wMonth,
               systime.wDay,
               systime.wYear,
               systime.wHour,
               systime.wMinute,
               systime.wSecond );
        break;
    case VT_I2:
        printf("%d\n", var.iVal );
        break;
    case VT_I4:
        printf("%d\n", var.lVal );
        break;
    default:
        printf("type is:%i\n", var.vt );
        break;
}
// done processing, clear resources
VariantClear( &var );
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">IEnumCERTVIEWCOLUMN::Next</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-reset">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-skip">IEnumCERTVIEWCOLUMN::Skip</a>