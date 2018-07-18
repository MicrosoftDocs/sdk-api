---
UID: NF:tapi3if.ITTerminalSupport.GetDefaultStaticTerminal
title: ITTerminalSupport::GetDefaultStaticTerminal
author: windows-sdk-content
description: The GetDefaultStaticTerminal method gets the default static terminal for the media type specified.
old-location: tapi3\itterminalsupport_getdefaultstaticterminal.htm
old-project: tapi
ms.assetid: aad3a566-eb95-402c-b26f-da6bd89e52ea
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: GetDefaultStaticTerminal, GetDefaultStaticTerminal method [TAPI 2.2], GetDefaultStaticTerminal method [TAPI 2.2],ITTerminalSupport interface, ITTerminalSupport interface [TAPI 2.2],GetDefaultStaticTerminal method, ITTerminalSupport.GetDefaultStaticTerminal, ITTerminalSupport::GetDefaultStaticTerminal, _tapi3_itterminalsupport_getdefaultstaticterminal, tapi3.itterminalsupport_getdefaultstaticterminal, tapi3if/ITTerminalSupport::GetDefaultStaticTerminal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport.GetDefaultStaticTerminal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalSupport::GetDefaultStaticTerminal


## -description


The 
<b>GetDefaultStaticTerminal</b> method gets the default static terminal for the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> specified.


## -parameters




### -param lMediaType [in]


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> of the required terminal.


### -param Direction [in]


<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor of the terminal direction.


### -param ppTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface. <b>NULL</b> if no terminal is available.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No terminal is available. *<i>ppTerminal</i> will be returned as <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not a valid media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to create the Terminal object.

</td>
</tr>
</table>
 




## -remarks



This method does not return dynamic terminals. For example, having a media type of TAPIMEDIATYPE_VIDEO and a terminal direction of TD_RENDER defines a dynamic terminal; this method will fail with those parameters.

The default static terminal returned by this method is one of the static terminals returned by 
<a href="https://msdn.microsoft.com/91fea706-9792-40e1-b812-f7578bc7968b">ITTerminalSupport::EnumerateStaticTerminals</a> or 
<a href="https://msdn.microsoft.com/f4cdd3f5-ca8c-4660-b37c-c38779a516dd">ITTerminalSupport::get_StaticTerminals</a>. Usually, the default terminal is the one selected as "preferred device" in Control Panel's "Sounds and Multimedia Properties" applet.

TAPI calls the <a href="https://msdn.microsoft.com/library/ms691379(v=VS.85).aspx">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by <b>ITTerminalSupport::GetDefaultStaticTerminal</b>. The application must call <a href="https://msdn.microsoft.com/library/ms682317(v=VS.85).aspx">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a>



<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a>



<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

