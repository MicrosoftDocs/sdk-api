---
UID: NF:certview.IEnumCERTVIEWCOLUMN.Next
title: IEnumCERTVIEWCOLUMN::Next (certview.h)
description: Moves to the next column in the column-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWCOLUMN interface [Security]","Next method","IEnumCERTVIEWCOLUMN.Next","IEnumCERTVIEWCOLUMN::Next","Next","Next method [Security]","Next method [Security]","IEnumCERTVIEWCOLUMN interface","_certsrv_ienumcertviewcolumn_next","certview/IEnumCERTVIEWCOLUMN::Next","security.ienumcertviewcolumn_next"]
old-location: security\ienumcertviewcolumn_next.htm
tech.root: security
ms.assetid: 4c77d1c7-af3a-4a7d-bf42-69be887c881e
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWCOLUMN interface [Security],Next method, IEnumCERTVIEWCOLUMN.Next, IEnumCERTVIEWCOLUMN::Next, Next, Next method [Security], Next method [Security],IEnumCERTVIEWCOLUMN interface, _certsrv_ienumcertviewcolumn_next, certview/IEnumCERTVIEWCOLUMN::Next, security.ienumcertviewcolumn_next
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
 - IEnumCERTVIEWCOLUMN::Next
 - certview/IEnumCERTVIEWCOLUMN::Next
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
 - IEnumCERTVIEWCOLUMN.Next
 - IEnumCERTVIEWCOLUMN.Next
---

# IEnumCERTVIEWCOLUMN::Next


## -description

The <b>Next</b> method moves to the next column in the column-enumeration sequence.

## -parameters

### -param pIndex [out]

A pointer to a variable that  contains the index value of the next column referenced by the column-enumeration sequence. If there are no more columns to enumerate, this variable is set to –1. This method will fail if <i>pIndex</i> is <b>NULL</b>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the next column in the column-enumeration sequence is now being referenced. If there are no more columns to enumerate, the method returns S_FALSE, and the <i>pIndex</i> parameter is set to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the index value of the column that is now referenced by the column-enumeration sequence. If there are no more columns to enumerate, the return value is –1.

## -remarks

Upon successful completion of this method, the information in the column can be obtained by calling one of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getname">IEnumCERTVIEWCOLUMN::GetName</a>: Retrieves the nonlocalized name of the column.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getdisplayname">IEnumCERTVIEWCOLUMN::GetDisplayName</a>: Retrieves the localized name of the column.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getvalue">IEnumCERTVIEWCOLUMN::GetValue</a>: Retrieves the data in the column.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-gettype">IEnumCERTVIEWCOLUMN::GetType</a>: Retrieves the type of data in the column.</li>
<li>
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getmaxlength">IEnumCERTVIEWCOLUMN::GetMaxLength</a>: Retrieves the maximum length, in bytes, of the column.</li>
</ul>

#### Examples


```cpp
LONG       nLength;
LONG       nType;
LONG       bIsindexed;
LONG       Index;

HRESULT    hr;

BSTR       bstrColName = NULL;

// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
// examine each column
while (S_OK == pEnumCol->Next(&Index))
{
    // determine database length
    hr = pEnumCol->GetMaxLength(&nLength);
    if (FAILED(hr))
    {
        printf("Failed GetMaxLength %x\n", hr);
        goto error;
    }

    // determine data type
    hr = pEnumCol->GetType(&nType);
    if (FAILED(hr))
    {
        printf("Failed GetType %x\n", hr);
        goto error;
    }

    // determine whether column is indexed
    hr = pEnumCol->IsIndexed(&bIsindexed);
    if (FAILED(hr))
    {
        printf("Failed IsIndexed %x\n", hr);
        goto error;
    }

    // retrieve column name
    hr = pEnumCol->GetName(&bstrColName);
    if (FAILED(hr))
    {
        printf("Failed GetName %x\n", hr);
        goto error;
    }

    // print this column's info on one line
    // print name and length
    printf("Column %ws has max length %d",
            bstrColName,
            nLength); 

    // print data type
    switch (nType)
    {
        case PROPTYPE_BINARY:
            printf(" Type is Binary");
            break;
        case PROPTYPE_DATE:
            printf(" Type is Date+Time");
            break;
        case PROPTYPE_LONG:
            printf(" Type is Signed long");
            break;
        case PROPTYPE_STRING:
            printf(" Type is Unicode String");
            break;
        default:
            printf(" Type is unknown");
            break;
    }

    // print index status
    printf(bIsindexed ? " Indexed" : " Not indexed");
    // print new line marker
    printf("\n");

}

error:

// done processing, clear resources
if (NULL != bstrColName)
    SysFreeString(bstrColName);
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getdisplayname">IEnumCERTVIEWCOLUMN::GetDisplayName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getmaxlength">IEnumCERTVIEWCOLUMN::GetMaxLength</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getname">IEnumCERTVIEWCOLUMN::GetName</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-gettype">IEnumCERTVIEWCOLUMN::GetType</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getvalue">IEnumCERTVIEWCOLUMN::GetValue</a>