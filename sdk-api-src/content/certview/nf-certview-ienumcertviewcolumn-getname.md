---
UID: NF:certview.IEnumCERTVIEWCOLUMN.GetName
title: IEnumCERTVIEWCOLUMN::GetName
author: windows-sdk-content
description: Retrieves the nonlocalized name of the current column in the column-enumeration sequence.
old-location: security\ienumcertviewcolumn_getname.htm
tech.root: seccrypto
ms.assetid: be76cec1-9ac0-4cc0-bddb-992b2d3590d7
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetName, GetName method [Security], GetName method [Security],IEnumCERTVIEWCOLUMN interface, IEnumCERTVIEWCOLUMN interface [Security],GetName method, IEnumCERTVIEWCOLUMN.GetName, IEnumCERTVIEWCOLUMN::GetName, _certsrv_ienumcertviewcolumn_getname, certview/IEnumCERTVIEWCOLUMN::GetName, security.ienumcertviewcolumn_getname
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
 - IEnumCERTVIEWCOLUMN.GetName
 - IEnumCERTVIEWCOLUMN.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWCOLUMN::GetName


## -description


The <b>GetName</b> method retrieves the nonlocalized name of the current column in the column-enumeration sequence.


## -parameters




### -param pstrOut [out]

A pointer to a variable of <b>BSTR</b> type that  contains the name of the column.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK  and the <i>pstrOut</i> parameter contains the name of the column.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrOut</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that contains the name of the column.




## -remarks



This method is used to retrieve the nonlocalized name of the  column currently referenced by the 
column-enumeration sequence.

If the column-enumeration sequence is not referencing a valid column, <b>GetName</b> will fail. Use one of the following methods to navigate through the enumeration:

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
<pre>BSTR       bstrColName = NULL;
HRESULT    hr;

// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
hr = pEnumCol-&gt;GetName(&amp;bstrColName);
if (S_OK == hr)
    printf("Column name is %ws\n", bstrColName);

// done processing, clear resources
if (NULL != bstrColName)
    SysFreeString(bstrColName);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/4c77d1c7-af3a-4a7d-bf42-69be887c881e">IEnumCERTVIEWCOLUMN::Next</a>



<a href="https://msdn.microsoft.com/0be00eb0-1a22-4849-95ca-276099bbfa74">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="https://msdn.microsoft.com/9a101e5b-a137-4e15-81b6-90e0fc14b887">IEnumCERTVIEWCOLUMN::Skip</a>
 

 

