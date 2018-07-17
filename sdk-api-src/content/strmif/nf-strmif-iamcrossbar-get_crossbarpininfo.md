---
UID: NF:strmif.IAMCrossbar.get_CrossbarPinInfo
title: IAMCrossbar::get_CrossbarPinInfo
author: windows-sdk-content
description: The get_CrossbarPinInfo method retrieves information about a specified pin.
old-location: dshow\iamcrossbar_get_crossbarpininfo.htm
old-project: DirectShow
ms.assetid: 29cda12e-a731-4995-8e0c-69dfcda6f158
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FALSE, IAMCrossbar interface [DirectShow],get_CrossbarPinInfo method, IAMCrossbar.get_CrossbarPinInfo, IAMCrossbar::get_CrossbarPinInfo, IAMCrossbarget_CrossbarPinInfo, TRUE, dshow.iamcrossbar_get_crossbarpininfo, get_CrossbarPinInfo, get_CrossbarPinInfo method [DirectShow], get_CrossbarPinInfo method [DirectShow],IAMCrossbar interface, strmif/IAMCrossbar::get_CrossbarPinInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMCrossbar.get_CrossbarPinInfo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMCrossbar::get_CrossbarPinInfo


## -description



The <code>get_CrossbarPinInfo</code> method retrieves information about a specified pin.




## -parameters




### -param IsInputPin [in]

Specifies the direction of the pin. Use one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Input pin

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Output pin

</td>
</tr>
</table>
 


### -param PinIndex [in]

Specifies the index of the pin.


### -param PinIndexRelated [out]

Pointer to a variable that receives the index of the related pin, or –1 if no pin is related to this pin. The <i>related pin</i> is a pin on the same filter, with the same direction; it typically represents the same physical jack or connector. For example, a video tuner and an audio tuner might be related pins. Typically, if two pins are related, you should route them together.


### -param PhysicalType [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/00635c01-f068-43b0-b7b6-d26f27886f71">PhysicalConnectorType</a> enumeration, indicating the pin's physical type.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Unknown physical type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



Output pins and input pins are both indexed from zero. To determine the number of output and input pins, call the <a href="https://msdn.microsoft.com/66ea86a6-82c3-4f91-a2d3-a08014f555be">IAMCrossbar::get_PinCounts</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9eef4923-62e7-475e-85e6-de8c1eefe483">IAMCrossbar Interface</a>



<a href="https://msdn.microsoft.com/6e8ee9c3-6776-498b-ad38-36f8172a27ae">Working with Crossbars</a>
 

 

