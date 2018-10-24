---
UID: NN:mmc.IConsolePowerSink
title: IConsolePowerSink
author: windows-sdk-content
description: The IConsolePowerSink interface monitors and responds to power management messages.
old-location: mmc\iconsolepowersink.htm
tech.root: mmc
ms.assetid: dd23c6dc-9219-4d13-b237-13405a2fcb5a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IConsolePowerSink, IConsolePowerSink interface [MMC], IConsolePowerSink interface [MMC],described, _slate_iconsolepowersink, mmc.iconsolepowersink, mmc/IConsolePowerSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Mmc.h
api_name:
 - IConsolePowerSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsolePowerSink interface


## -description


The 
<b>IConsolePowerSink</b> interface monitors and responds to power management messages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsolePowerSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConsolePowerSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsolePowerSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69589335-4b80-4f2b-a8d6-74805969c85c">OnPowerBroadcast</a>
</td>
<td align="left" width="63%">
Handles 
WM_POWERBROADCAST messages.

</td>
</tr>
</table> 


## -remarks



To receive power management notifications, your snap-in must use the <a href="Http://go.microsoft.com/fwlink/p/?linkid=83932">AtlAdvise</a> function to associate an instance of the 
<a href="https://msdn.microsoft.com/d34e8da0-2689-4514-be10-4c11008432b3">IConsolePower</a> interface with your implementation of the 
<b>IConsolePowerSink</b> interface. The following code example shows how to use the <a href="Http://go.microsoft.com/fwlink/p/?linkid=83932">AtlAdvise</a> function.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Connect the IConsolePower and IConsolePowerSink interfaces.
// m_ipConsolePower is a pointer to an instance of 
// the IConsolePower interface.
// m_ipConsolePowerSink is a pointer to an instance of 
// the IConsolePowerSink interface.
// m_dwCookie is of type DWORD.
hr = AtlAdvise(m_ipConsolePower,
               m_ipConsolePowerSink,
               IID_IConsolePowerSink,
               &amp;m_dwCookie);</pre>
</td>
</tr>
</table></span></div>
When your snap-in closes or no longer requires power management notifications, call the <a href="Http://go.microsoft.com/fwlink/p/?linkid=83933">AtlUnadvise</a> function to terminate the connection between the 
IConsolePower and 
IConsolePowerSink interfaces. The following code example shows how to use the <a href="Http://go.microsoft.com/fwlink/p/?linkid=83933">AtlUnadvise</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Terminate the connection established previously.
hr = AtlUnadvise(m_ipConsolePower,
                 IID_IConsolePowerSink,
                 m_dwCookie);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d34e8da0-2689-4514-be10-4c11008432b3">IConsolePower</a>
 

 

