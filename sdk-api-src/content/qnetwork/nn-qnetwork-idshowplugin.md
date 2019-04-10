---
UID: NN:qnetwork.IDShowPlugin
title: IDShowPlugin (qnetwork.h)
author: windows-sdk-content
description: The IDShowPlugin interface enables the Windows Media Source filter to communicate with the Windows Media Player 6.4 Plug-in for Netscape Navigator.
old-location: dshow\idshowplugin.htm
tech.root: DirectShow
ms.assetid: b5b73489-4d2d-4afa-a4df-7b84711f2556
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDShowPlugin, IDShowPlugin interface [DirectShow], IDShowPlugin interface [DirectShow],described, IDShowPluginInterface, dshow.idshowplugin, qnetwork/IDShowPlugin
ms.topic: interface
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IDShowPlugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDShowPlugin interface


## -description



The <b>IDShowPlugin</b> interface enables the <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter to communicate with the Windows Media Player 6.4 Plug-in for Netscape Navigator. If Windows Media Player 6.4 is hosted in the Netscape Navigator browser, the Windows Media Source filter uses this interface to retrieve the URL and the User-Agent heading. This interface is not used when the player is hosted as an ActiveX control in Microsoft Internet Explorer.

Applications cannot access this interface. It is documented here for completeness, because it is defined in the header file Qnetwork.h.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDShowPlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDShowPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDShowPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406855(v=VS.85).aspx">get_URL</a>
</td>
<td align="left" width="63%">
Gets the URL of the current web page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406856(v=VS.85).aspx">get_UserAgent</a>
</td>
<td align="left" width="63%">
Gets the User-Agent string.

</td>
</tr>
</table> 


## -remarks



To define the interface identifier, include the header file Initguid.h before Qnetwork.h, but after Dshow.h and other header files:

<pre class="syntax" xml:space="preserve"><code>#include &lt;dshow.h&gt;
#include &lt;initguid.h&gt;
#include &lt;qnetwork.h&gt;
</code></pre>
<div class="alert"><b>Note</b>  Make sure that Initguid.h is included only once in your project. Otherwise, you will receive linker errors for duplicate GUID values.</div>
<div> </div>


