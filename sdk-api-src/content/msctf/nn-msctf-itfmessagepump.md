---
UID: NN:msctf.ITfMessagePump
title: ITfMessagePump
author: windows-sdk-content
description: The ITfMessagePump interface is implemented by the TSF manager and is used by an application to obtain messages from the application message queue.
old-location: tsf\itfmessagepump.htm
tech.root: TSF
ms.assetid: f7c3d039-cffc-4ce0-8579-041ba849de6d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfMessagePump, ITfMessagePump interface [Text Services Framework], ITfMessagePump interface [Text Services Framework],described, _tsf_itfmessagepump_ref, msctf/ITfMessagePump, tsf.itfmessagepump
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfMessagePump
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfMessagePump interface


## -description


The <b>ITfMessagePump</b> interface is implemented by the TSF manager and is used by an application to obtain messages from the application message queue. The methods of this interface are wrappers for the <a href="_win32_getmessage">GetMessage</a> and <a href="_win32_peekmessage">PeekMessage</a> functions. This interface enables the TSF manager to perform any necessary pre-message or post-message processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMessagePump</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfMessagePump</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMessagePump</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1d66377-fca1-4c9c-ac59-a1417d8ab190">GetMessageA</a>
</td>
<td align="left" width="63%">
Obtains a message from the message queue and does not return until a message is obtained. This is the ANSI version of this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2283d04-f5b8-4b86-9fa5-517e46417b07">GetMessageW</a>
</td>
<td align="left" width="63%">
Obtains a message from the message queue and does not return until a message is obtained. This is the Unicode version of this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b20fa18-f5c3-4f3b-bb93-0e352d620d31">PeekMessageA</a>
</td>
<td align="left" width="63%">
Obtains a message from the message queue and returns if no message is obtained. This is the ANSI version of this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05a3a7e1-4b83-4257-bfe8-7f79405ff02a">PeekMessageW</a>
</td>
<td align="left" width="63%">
Obtains a message from the message queue and returns if no message is obtained. This is the Unicode version of this method.

</td>
</tr>
</table> 


## -remarks



If the application is Unicode, it should use the PeekMessageW and GetMessageW methods. Otherwise, the application should use the PeekMessageA and GetMessageA methods.


#### Examples


<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr
          </a>


<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfMessagePump *pMessagePump;

hr = pThreadManager-&gt;QueryInterface(IID_ITfMessagePump, (LPVOID*)&amp;pMessagePump);
if(SUCCEEDED(hr))
{
    //Use the ITfMessagePump interface. 
    
    //Release the ITfMessagePump interface. 
    pMessagePump-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>


