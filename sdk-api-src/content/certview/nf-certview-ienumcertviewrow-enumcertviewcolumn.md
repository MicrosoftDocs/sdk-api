---
UID: NF:certview.IEnumCERTVIEWROW.EnumCertViewColumn
title: IEnumCERTVIEWROW::EnumCertViewColumn
author: windows-sdk-content
description: Obtains an instance of a column-enumeration sequence for the current row of the row-enumeration sequence.
old-location: security\ienumcertviewrow_enumcertviewcolumn.htm
tech.root: seccrypto
ms.assetid: 78fd2431-c4c7-4df9-856a-69665fa8c063
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EnumCertViewColumn, EnumCertViewColumn method [Security], EnumCertViewColumn method [Security],IEnumCERTVIEWROW interface, IEnumCERTVIEWROW interface [Security],EnumCertViewColumn method, IEnumCERTVIEWROW.EnumCertViewColumn, IEnumCERTVIEWROW::EnumCertViewColumn, _certsrv_ienumcertviewrow_enumcertviewcolumn, certview/IEnumCERTVIEWROW::EnumCertViewColumn, security.ienumcertviewrow_enumcertviewcolumn
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
 - IEnumCERTVIEWROW.EnumCertViewColumn
 - IEnumCERTVIEWROW.EnumCertViewColumn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWROW::EnumCertViewColumn


## -description


The <b>EnumCertViewColumn</b> method obtains an instance of a column-enumeration sequence for the current row of the row-enumeration sequence.


## -parameters




### -param ppenum [out]

A pointer to a pointer of <a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a> type.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a column-enumeration sequence object.




## -remarks



The 
column-enumeration sequence obtained by this call can be used to enumerate the columns associated with the certificate in the current row. This enumeration can be accessed through the methods of the <a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a> interface.

To reference a different row, call one of the following methods to navigate through the row-enumeration sequence:

<ul>
<li>
<a href="https://msdn.microsoft.com/76bee5db-0443-4673-a59c-0198587736dc">IEnumCERTVIEWROW::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/6e471ee9-4b69-468c-a724-e43bd93419d9">IEnumCERTVIEWROW::Next</a>: Moves to the next row in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/9115262e-00bb-4446-906d-7a57fd5781d1">IEnumCERTVIEWROW::Skip</a>: Skips a specified number of rows.</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW
HRESULT               hr;
LONG                  Index;
IEnumCERTVIEWCOLUMN * pEnumCol = NULL;
// obtain enumerator for columns
hr = pEnumRow-&gt;EnumCertViewColumn(&amp;pEnumCol);
if ( FAILED( hr ))
{
    printf("Failed EnumCertViewColumn - %x\n", hr );
    goto error;
}
// enumerate each column
while (S_OK == pEnumCol-&gt;Next(&amp;Index))
{
    // Use this column as needed.
}
error:

// Free resources.
if ( NULL != pEnumCol )
    pEnumCol-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/c9529f7a-9d97-4315-af96-f7b687af3c2e">IEnumCERTVIEWROW</a>



<a href="https://msdn.microsoft.com/6e471ee9-4b69-468c-a724-e43bd93419d9">IEnumCERTVIEWROW::Next</a>



<a href="https://msdn.microsoft.com/76bee5db-0443-4673-a59c-0198587736dc">IEnumCERTVIEWROW::Reset</a>



<a href="https://msdn.microsoft.com/9115262e-00bb-4446-906d-7a57fd5781d1">IEnumCERTVIEWROW::Skip</a>
 

 

