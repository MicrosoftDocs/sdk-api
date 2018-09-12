---
UID: NF:certview.IEnumCERTVIEWCOLUMN.GetType
title: IEnumCERTVIEWCOLUMN::GetType
author: windows-sdk-content
description: Retrieves the data type of the current column in the column-enumeration sequence.
old-location: security\ienumcertviewcolumn_gettype.htm
tech.root: seccrypto
ms.assetid: 53297e9e-6583-4edf-85f4-e2b2e4ba28b3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetType, GetType method [Security], GetType method [Security],IEnumCERTVIEWCOLUMN interface, IEnumCERTVIEWCOLUMN interface [Security],GetType method, IEnumCERTVIEWCOLUMN.GetType, IEnumCERTVIEWCOLUMN::GetType, _certsrv_ienumcertviewcolumn_gettype, certview/IEnumCERTVIEWCOLUMN::GetType, security.ienumcertviewcolumn_gettype
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
 - IEnumCERTVIEWCOLUMN.GetType
 - IEnumCERTVIEWCOLUMN.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWCOLUMN::GetType


## -description


The <b>GetType</b> method retrieves the data type of the current column in the column-enumeration sequence.


## -parameters




### -param pType [out]

A pointer to a variable of <b>LONG</b> type that denotes the data type of the column referenced by the column-enumeration sequence.  For a table of the valid data types, see Remarks. This method  fails if the <i>pType</i> parameter is set to <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value represents the data type of the column. For a table of the valid data types, see Remarks.




## -remarks



This method is used to determine the data type of the  column currently referenced by the 
column-enumeration sequence. The valid data types are listed in the following table.

<table>
<tr>
<th>Data type</th>
<th>Meaning</th>
</tr>
<tr>
<td>PROPTYPE_BINARY</td>
<td>Binary data</td>
</tr>
<tr>
<td>PROPTYPE_DATE</td>
<td>Date/time</td>
</tr>
<tr>
<td>PROPTYPE_LONG</td>
<td>Signed long</td>
</tr>
<tr>
<td>PROPTYPE_STRING</td>
<td><a href="https://msdn.microsoft.com/en-us/library/ms721629(v=VS.85).aspx">Unicode</a> string</td>
</tr>
</table>
 

If the column-enumeration sequence is not referencing a valid column, <b>GetType</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386199(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386197(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Next</a>: Moves to the next column in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386201(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Skip</a>: Skips a specified number of columns.</li>
</ul>

#### Examples


```cpp
LONG     nType;
HRESULT  hr;

// pEnumCol is a previously instantiated IEnumCERTVIEWCOLUMN object.
hr = pEnumCol->GetType(&nType);
if (S_OK == hr)
{
    switch (nType)
    {
        case PROPTYPE_BINARY:
            printf("Type is Binary\n");
            break;
        case PROPTYPE_DATE:
            printf("Type is Date+Time\n");
            break;
        case PROPTYPE_LONG:
            printf("Type is Signed long\n");
            break;
        case PROPTYPE_STRING:
            printf("Type is Unicode String\n");
            break;
        default:
            printf("Type is unknown\n");
            break;
    }
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386176(v=VS.85).aspx">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386197(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Next</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386199(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386201(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Skip</a>
 

 

