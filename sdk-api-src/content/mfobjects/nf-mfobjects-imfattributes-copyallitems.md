---
UID: NF:mfobjects.IMFAttributes.CopyAllItems
title: IMFAttributes::CopyAllItems
author: windows-sdk-content
description: Copies all of the attributes from this object into another attribute store.
old-location: mf\imfattributes_copyallitems.htm
tech.root: medfound
ms.assetid: 111b55bc-fb8e-45b5-a709-703acd23c4be
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 111b55bc-fb8e-45b5-a709-703acd23c4be, CopyAllItems, CopyAllItems method [Media Foundation], CopyAllItems method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],CopyAllItems method, IMFAttributes.CopyAllItems, IMFAttributes::CopyAllItems, mf.imfattributes_copyallitems, mfobjects/IMFAttributes::CopyAllItems
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.CopyAllItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAttributes::CopyAllItems


## -description


Copies all of the attributes from this object into another attribute store.
        


## -parameters




### -param pDest [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store that receives the copy.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method deletes all of the attributes originally stored in <i>pDest</i>.
      

<div class="alert"><b>Note</b>  <p class="note">When you call <b>CopyAllItems</b> on an <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>, which inherits this method, the sample time, duration, and flags are not copied to the destination sample. You must copy these values to the new sample manually.

</div>
<div> </div>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

To copy a single attribute rather than all of the attributes, you can use the following code:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CopyAttribute(IMFAttributes *pFrom, IMFAttributes *pTo, REFGUID guidKey)
{
    PROPVARIANT val;

    HRESULT hr = pFrom-&gt;GetItem(guidKey, &amp;val);

    if (SUCCEEDED(hr))
    {
        hr = pTo-&gt;SetItem(guidKey, val);
        PropVariantClear(&amp;val);
    }
    else if (hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = S_OK;
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 

