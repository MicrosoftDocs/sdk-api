---
UID: NF:mfobjects.IMFAttributes.GetItem
title: IMFAttributes::GetItem
author: windows-sdk-content
description: Retrieves the value associated with a key.
old-location: mf\imfattributes_getitem.htm
old-project: medfound
ms.assetid: 8cc4e529-d5a0-4342-82ac-ae5b28bfd61d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 8cc4e529-d5a0-4342-82ac-ae5b28bfd61d, GetItem, GetItem method [Media Foundation], GetItem method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetItem method, IMFAttributes.GetItem, IMFAttributes::GetItem, mf.imfattributes_getitem, mfobjects/IMFAttributes::GetItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.GetItem
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAttributes::GetItem


## -description



Retrieves the value associated with a key.




## -parameters




### -param guidKey [in]


            A GUID that identifies which value to retrieve.
          


### -param pValue [in, out]

A pointer to a <b>PROPVARIANT</b> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value, if the value is found. Call <b>PropVariantClear</b> to free the memory allocated by this method. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the method searches for the key and returns S_OK if the key is found, but does not copy the value.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">

                The specified key was not found.
              

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following example copies an attribute from one attribute store to another.

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
 

 

