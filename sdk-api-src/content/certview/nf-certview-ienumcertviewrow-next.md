---
UID: NF:certview.IEnumCERTVIEWROW.Next
title: IEnumCERTVIEWROW::Next
author: windows-sdk-content
description: Moves to the next row in the row-enumeration sequence.
old-location: security\ienumcertviewrow_next.htm
tech.root: SecCrypto
ms.assetid: 6e471ee9-4b69-468c-a724-e43bd93419d9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnumCERTVIEWROW interface [Security],Next method, IEnumCERTVIEWROW.Next, IEnumCERTVIEWROW::Next, Next, Next method [Security], Next method [Security],IEnumCERTVIEWROW interface, _certsrv_ienumcertviewrow_next, certview/IEnumCERTVIEWROW::Next, security.ienumcertviewrow_next
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
 - IEnumCERTVIEWROW.Next
 - IEnumCERTVIEWROW.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certview.h
: 
- IEnumCERTVIEWROW.Next
: 
---

# IEnumCERTVIEWROW::Next


## -description


The <b>Next</b> method moves to the next row in the row-enumeration sequence.


## -parameters




### -param pIndex [out]

A pointer to a variable that contains the index value of the next row being  referenced. If there are no more rows to enumerate, this variable will be set to –1. This method fails if <i>pIndex</i> is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the next row is now being referenced by the row-enumeration sequence. If there are no more rows to enumerate, S_FALSE is returned, and <i>pIndex</i> is set to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the index value of the  row that is now being referenced by the row-enumeration sequence. If there are no more rows to enumerate, the return value is –1.




## -remarks



Upon successful completion of this method, the 
columns, attributes, and extensions associated with the certificate in the row can be enumerated using the methods of the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a>
</li>
</ul>
Looping through all the  rows in the enumeration sequence can be resource-intensive to compute, depending of the query involved and the  size of the sequence.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW.
LONG  Index;
LONG  nCount;

// Ensure enumerator is at first row.
if (FAILED(pEnumRow-&gt;Reset()))
    printf("Failed to Reset\n");
else
{
    nCount = 0;
    // Count the database records by enumerating the rows.
    while (S_OK == pEnumRow-&gt;Next(&amp;Index))
        nCount++;
    // Display number of records.
    printf("Number of records is %d\n", nCount);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>



<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a>



<a href="https://msdn.microsoft.com/c9529f7a-9d97-4315-af96-f7b687af3c2e">IEnumCERTVIEWROW</a>
 

 

