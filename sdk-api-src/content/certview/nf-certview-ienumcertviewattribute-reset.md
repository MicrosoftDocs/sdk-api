---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.Reset
title: IEnumCERTVIEWATTRIBUTE::Reset
author: windows-sdk-content
description: Moves to the beginning of the attribute-enumeration sequence.
old-location: security\ienumcertviewattribute_reset.htm
tech.root: seccrypto
ms.assetid: 1f5b8ee0-2820-481b-8836-b2926aec0933
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CEnumCERTVIEWATTRIBUTE object [Security],Reset method, IEnumCERTVIEWATTRIBUTE interface [Security],Reset method, IEnumCERTVIEWATTRIBUTE.Reset, IEnumCERTVIEWATTRIBUTE::Reset, Reset, Reset method [Security], Reset method [Security],CEnumCERTVIEWATTRIBUTE object, Reset method [Security],IEnumCERTVIEWATTRIBUTE interface, _certsrv_ienumcertviewattribute_reset, certview/IEnumCERTVIEWATTRIBUTE::Reset, security.ienumcertviewattribute_reset
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
 - IEnumCERTVIEWATTRIBUTE.Reset
 - CEnumCERTVIEWATTRIBUTE.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWATTRIBUTE::Reset


## -description


The <b>Reset</b> method moves to the beginning of the attribute-enumeration sequence.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, call the 
<a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE::Next</a> method to reference the first attribute in the attribute-enumeration sequence.  The attribute name and value can be accessed by using the 
following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/c2409bf1-0571-479e-8499-010d52cfb776">IEnumCERTVIEWATTRIBUTE::GetName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a03a6da4-d286-487e-a292-8a02626325a8">IEnumCERTVIEWATTRIBUTE::GetValue</a>
</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumAttr is a previously instantiated
// IEnumCERTVIEWATTRIBUTE object.
HRESULT  hr;
LONG     Index;

hr = pEnumAttr-&gt;Reset();
if (S_OK != hr)
    printf("Unable to reset pEnumAttr - %x\n", hr );


    // Call the appropriate error handler and exit routine.
else
{

    // Reset to the beginning of the attributes again.
    while (S_OK == pEnumAttr-&gt;Next(&amp;Index))
    {

        // Use each attribute as needed.
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>



<a href="https://msdn.microsoft.com/c2409bf1-0571-479e-8499-010d52cfb776">IEnumCERTVIEWATTRIBUTE::GetName</a>



<a href="https://msdn.microsoft.com/a03a6da4-d286-487e-a292-8a02626325a8">IEnumCERTVIEWATTRIBUTE::GetValue</a>



<a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE::Next</a>



<a href="https://msdn.microsoft.com/546e7ad7-73f2-4f6e-8d02-a9ca5401ecce">IEnumCERTVIEWATTRIBUTE::Skip</a>
 

 

