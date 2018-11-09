---
UID: NF:certview.IEnumCERTVIEWCOLUMN.GetType
title: IEnumCERTVIEWCOLUMN::GetType
author: windows-sdk-content
description: Retrieves the data type of the current column in the column-enumeration sequence.
old-location: security\ienumcertviewcolumn_gettype.htm
tech.root: seccrypto
ms.assetid: 53297e9e-6583-4edf-85f4-e2b2e4ba28b3
ms.author: windowssdkdev
ms.date: 11/08/2018
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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
<td><a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string</td>
</tr>
</table>
 

If the column-enumeration sequence is not referencing a valid column, <b>GetType</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="https://msdn.microsoft.com/0be00eb0-1a22-4849-95ca-276099bbfa74">IEnumCERTVIEWCOLUMN::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/4c77d1c7-af3a-4a7d-bf42-69be887c881e">IEnumCERTVIEWCOLUMN::Next</a>: Moves to the next column in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/9a101e5b-a137-4e15-81b6-90e0fc14b887">IEnumCERTVIEWCOLUMN::Skip</a>: Skips a specified number of columns.</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LONG     nType;
HRESULT  hr;

// pEnumCol is a previously instantiated IEnumCERTVIEWCOLUMN object.
hr = pEnumCol-&gt;GetType(&amp;nType);
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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/4c77d1c7-af3a-4a7d-bf42-69be887c881e">IEnumCERTVIEWCOLUMN::Next</a>



<a href="https://msdn.microsoft.com/0be00eb0-1a22-4849-95ca-276099bbfa74">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="https://msdn.microsoft.com/9a101e5b-a137-4e15-81b6-90e0fc14b887">IEnumCERTVIEWCOLUMN::Skip</a>
 

 

