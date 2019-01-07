---
UID: NF:certview.IEnumCERTVIEWCOLUMN.GetMaxLength
title: IEnumCERTVIEWCOLUMN::GetMaxLength
author: windows-sdk-content
description: Retrieves the maximum allowable length, in bytes, for the column data.
old-location: security\ienumcertviewcolumn_getmaxlength.htm
tech.root: SecCrypto
ms.assetid: 20cd5f5a-2e19-43ca-9b84-70e6dd1a4cad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMaxLength, GetMaxLength method [Security], GetMaxLength method [Security],IEnumCERTVIEWCOLUMN interface, IEnumCERTVIEWCOLUMN interface [Security],GetMaxLength method, IEnumCERTVIEWCOLUMN.GetMaxLength, IEnumCERTVIEWCOLUMN::GetMaxLength, _certsrv_ienumcertviewcolumn_getmaxlength, certview/IEnumCERTVIEWCOLUMN::GetMaxLength, security.ienumcertviewcolumn_getmaxlength
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
 - IEnumCERTVIEWCOLUMN.GetMaxLength
 - IEnumCERTVIEWCOLUMN.GetMaxLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWCOLUMN::GetMaxLength


## -description


The <b>GetMaxLength</b> method retrieves the maximum allowable length, in bytes, for the column data.

 If the column data's type is <b>PROPTYPE_STRING</b>, divide the number of bytes by <code>sizeof(WCHAR)</code> to determine the maximum number of <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> characters.


## -parameters




### -param pMaxLength [out]

A pointer to a value of <b>LONG</b> type  that  contains the maximum allowable length for the column data. This function will fail if <i>pMaxLength</i> is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the <i>pMaxLength</i> is set to the  maximum allowable length for the column data.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the maximum allowable length, in bytes, for the column data.




## -remarks



This method is used to determine the maximum allowable data length for the column currently being referenced by the 
column-enumeration sequence.

If the column-enumeration sequence is not referencing a valid column, <b>GetMaxLength</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="https://msdn.microsoft.com/0be00eb0-1a22-4849-95ca-276099bbfa74">IEnumCERTVIEWCOLUMN::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/4c77d1c7-af3a-4a7d-bf42-69be887c881e">IEnumCERTVIEWCOLUMN::Next</a>: Moves to the next column in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/9a101e5b-a137-4e15-81b6-90e0fc14b887">IEnumCERTVIEWCOLUMN::Skip</a>: Skips a specified number of columns.</li>
</ul>
To determine whether the column data is indexed, call the <a href="https://msdn.microsoft.com/7373c0c3-3a1d-4a32-90e6-0f0575a0b61b">IEnumCERTVIEWCOLUMN::IsIndexed</a> method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
HRESULT  hr;
LONG     nLength;

// determine database length
hr = pEnumCol-&gt;GetMaxLength(&amp;nLength);
if (S_OK == hr)
    printf("max length is %d\n", nLength);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/7373c0c3-3a1d-4a32-90e6-0f0575a0b61b">IEnumCERTVIEWCOLUMN::IsIndexed</a>



<a href="https://msdn.microsoft.com/4c77d1c7-af3a-4a7d-bf42-69be887c881e">IEnumCERTVIEWCOLUMN::Next</a>



<a href="https://msdn.microsoft.com/0be00eb0-1a22-4849-95ca-276099bbfa74">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="https://msdn.microsoft.com/9a101e5b-a137-4e15-81b6-90e0fc14b887">IEnumCERTVIEWCOLUMN::Skip</a>
 

 

