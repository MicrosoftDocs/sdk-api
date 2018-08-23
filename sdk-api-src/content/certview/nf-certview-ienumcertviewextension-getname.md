---
UID: NF:certview.IEnumCERTVIEWEXTENSION.GetName
title: IEnumCERTVIEWEXTENSION::GetName
author: windows-sdk-content
description: Retrieves the name of the current extension in the extension-enumeration sequence.
old-location: security\ienumcertviewextension_getname.htm
old-project: SecCrypto
ms.assetid: 7c56708c-ae25-46f5-94f3-d58eea8d08d4
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CEnumCERTVIEWEXTENSION object [Security],GetName method, GetName, GetName method [Security], GetName method [Security],CEnumCERTVIEWEXTENSION object, GetName method [Security],IEnumCERTVIEWEXTENSION interface, IEnumCERTVIEWEXTENSION interface [Security],GetName method, IEnumCERTVIEWEXTENSION.GetName, IEnumCERTVIEWEXTENSION::GetName, _certsrv_ienumcertviewextension_getname, certview/IEnumCERTVIEWEXTENSION::GetName, security.ienumcertviewextension_getname
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
 - IEnumCERTVIEWEXTENSION.GetName
 - CEnumCERTVIEWEXTENSION.GetName
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# IEnumCERTVIEWEXTENSION::GetName


## -description


The <b>GetName</b> method retrieves the name of the current extension in the extension-enumeration sequence.

 The returned extension name is an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) string, as in L"2.5.29.31".


## -parameters




### -param pstrOut [out]

A pointer to a value of <b>BSTR</b> type that contains the name of the extension.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and tat the <i>pstrOut</i> parameter is set to the name of the extension.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrOut</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that contains the name of the extension.




## -remarks



This function is used to retrieve the name of the extension currently referenced by the 
extension-enumeration sequence.

If the extension-enumeration sequence is not referencing a valid extension, <b>GetName</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386225(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Reset</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386220(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Next</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386227(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Skip</a>: Skips a specified number of extensions.</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR  bstrExtName = NULL;

// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
hr = pEnumExt-&gt;GetName(&amp;bstrExtName);
if (S_OK == hr)
    printf("Extension name is: %ws\n", bstrExtName);
else
    printf("GetName failed: %x\n", hr);

// free memory when done
if (NULL != bstrExtName)
    SysFreeString(bstrExtName);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386203(v=VS.85).aspx">IEnumCERTVIEWEXTENSION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386208(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386216(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetValue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386220(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Next</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386225(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Reset</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386227(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Skip</a>
 

 

