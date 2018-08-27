---
UID: NF:certview.IEnumCERTVIEWCOLUMN.Next
title: IEnumCERTVIEWCOLUMN::Next
author: windows-sdk-content
description: Moves to the next column in the column-enumeration sequence.
old-location: security\ienumcertviewcolumn_next.htm
old-project: SecCrypto
ms.assetid: 4c77d1c7-af3a-4a7d-bf42-69be887c881e
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IEnumCERTVIEWCOLUMN interface [Security],Next method, IEnumCERTVIEWCOLUMN.Next, IEnumCERTVIEWCOLUMN::Next, Next, Next method [Security], Next method [Security],IEnumCERTVIEWCOLUMN interface, _certsrv_ienumcertviewcolumn_next, certview/IEnumCERTVIEWCOLUMN::Next, security.ienumcertviewcolumn_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certview.h
req.include-header: Certsrv.h
req.redist: 
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
req.typenames: ENUM_CATYPES
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
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the index value of the column that is now referenced by the column-enumeration sequence. If there are no more columns to enumerate, the return value is –1.




## -remarks



Upon successful completion of this method, the information in the column can be obtained by calling one of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386186(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetName</a>: Retrieves the nonlocalized name of the column.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386182(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetDisplayName</a>: Retrieves the localized name of the column.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386192(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetValue</a>: Retrieves the data in the column.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386189(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetType</a>: Retrieves the type of data in the column.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386184(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetMaxLength</a>: Retrieves the maximum length, in bytes, of the column.</li>
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




<a href="https://msdn.microsoft.com/en-us/library/Aa386176(v=VS.85).aspx">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386182(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetDisplayName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386184(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetMaxLength</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386186(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386189(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetType</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386192(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetValue</a>
 

 

