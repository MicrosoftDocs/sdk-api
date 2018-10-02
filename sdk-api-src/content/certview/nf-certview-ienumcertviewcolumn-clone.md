---
UID: NF:certview.IEnumCERTVIEWCOLUMN.Clone
title: IEnumCERTVIEWCOLUMN::Clone
author: windows-sdk-content
description: Creates a copy of the column-enumeration sequence.
old-location: security\ienumcertviewcolumn_clone.htm
tech.root: seccrypto
ms.assetid: a0870155-3f16-4cfb-b180-7a8e617dfcd8
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: Clone, Clone method [Security], Clone method [Security],IEnumCERTVIEWCOLUMN interface, IEnumCERTVIEWCOLUMN interface [Security],Clone method, IEnumCERTVIEWCOLUMN.Clone, IEnumCERTVIEWCOLUMN::Clone, _certsrv_ienumcertviewcolumn_clone, certview/IEnumCERTVIEWCOLUMN::Clone, security.ienumcertviewcolumn_clone
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
 - IEnumCERTVIEWCOLUMN.Clone
 - IEnumCERTVIEWCOLUMN.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWCOLUMN::Clone


## -description


The <b>Clone</b> method creates a copy of the column-enumeration sequence.


## -parameters




### -param ppenum [out]

A pointer to a pointer of <a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a> type. This method will fail if the <i>ppenum</i> is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a cloned column-enumeration sequence object.




## -remarks



The column-enumeration sequence is obtained by a call to the <a href="https://msdn.microsoft.com/78fd2431-c4c7-4df9-856a-69665fa8c063">IEnumCERTVIEWROW::EnumCertViewColumn</a> method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
IEnumCERTVIEWCOLUMN * pEnumCol2 = NULL;
HRESULT    hr;
hr = pEnumCol-&gt;Clone(&amp;pEnumCol2);
if (S_OK != hr)
    printf("Unable to clone IEnumCERTVIEWCOLUMN\n");
else
{
    // use cloned object as needed
    // ...
    // done using cloned object, free memory
}
if (NULL != pEnumCol2)
    pEnumCol2-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/78fd2431-c4c7-4df9-856a-69665fa8c063">IEnumCERTVIEWROW::EnumCertViewColumn</a>
 

 

