---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

