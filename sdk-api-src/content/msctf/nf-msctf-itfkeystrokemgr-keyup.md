---
UID: NF:msctf.ITfKeystrokeMgr.KeyUp
title: ITfKeystrokeMgr::KeyUp (msctf.h)
author: windows-sdk-content
description: ITfKeystrokeMgr::KeyUp method
old-location: tsf\itfkeystrokemgr_keyup.htm
tech.root: TSF
ms.assetid: 14415de3-f397-4866-b7d1-167c0931a80c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],KeyUp method, ITfKeystrokeMgr.KeyUp, ITfKeystrokeMgr::KeyUp, KeyUp, KeyUp method [Text Services Framework], KeyUp method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_keyup_ref, msctf/ITfKeystrokeMgr::KeyUp, tsf.itfkeystrokemgr_keyup
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - Msctf.dll
api_name:
 - ITfKeystrokeMgr.KeyUp
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfKeystrokeMgr::KeyUp


## -description




## -parameters




### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>.


### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>.


### -param pfEaten [out]

Pointer to a BOOL that, on exit, indicates if the key event will be handled. If this value receives <b>TRUE</b>, the key event would be handled and the event should not be forwarded to the application. If this value is <b>FALSE</b>, the key event would not be handled and the event should be forwarded to the application.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No key event sinks are installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



If this method is successful and <i>pfEaten</i> receives <b>TRUE</b>, the application should not process the key down event. If this method does not return S_OK or <i>pfEaten</i> receives <b>FALSE</b>, the application should process the key down event. The following is an example of how this is implemented.

<pre class="syntax" xml:space="preserve"><code>
if(msg.message == WM_KEYUP)
{
    if( pKeyboardMgr-&gt;TestKeyUp(msg.wParam, msg.lParam, &amp;fEaten) == S_OK 
        &amp;&amp; fEaten 
        &amp;&amp; pKeyboardMgr-&gt;KeyUp(msg.wParam, msg.lParam, &amp;fEaten) == S_OK 
        &amp;&amp; fEaten)
    {
        //The key was handled by the keystroke manager or a TSF text service. Do not pass the key to the application. 
        continue;
    }
    else
    {
        //Let the application process the key. 
    }
}
</code></pre>
If the keystroke manager does not handle the key event, it passes the key event to the text services by a call to the text service <a href="https://msdn.microsoft.com/5718a15b-985e-4286-a963-cee513e7550c">ITfKeyEventSink::OnKeyUp</a> method.




## -see-also




<a href="https://msdn.microsoft.com/5718a15b-985e-4286-a963-cee513e7550c">ITfKeyEventSink::OnKeyUp</a>



<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>



<a href="https://msdn.microsoft.com/6eb4ad91-9431-4dec-b6cb-e58707318095">ITfKeystrokeMgr::KeyDown</a>



<a href="https://msdn.microsoft.com/34a2b34b-3c3d-4609-a9e1-9b01ab349ae7">ITfKeystrokeMgr::TestKeyUp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>
 

 

