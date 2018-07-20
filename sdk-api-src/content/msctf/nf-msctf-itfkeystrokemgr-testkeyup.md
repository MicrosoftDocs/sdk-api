---
UID: NF:msctf.ITfKeystrokeMgr.TestKeyUp
title: ITfKeystrokeMgr::TestKeyUp
author: windows-sdk-content
description: ITfKeystrokeMgr::TestKeyUp method
old-location: tsf\itfkeystrokemgr_testkeyup.htm
old-project: TSF
ms.assetid: 34a2b34b-3c3d-4609-a9e1-9b01ab349ae7
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],TestKeyUp method, ITfKeystrokeMgr.TestKeyUp, ITfKeystrokeMgr::TestKeyUp, TestKeyUp, TestKeyUp method [Text Services Framework], TestKeyUp method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_testkeyup_ref, msctf/ITfKeystrokeMgr::TestKeyUp, tsf.itfkeystrokemgr_testkeyup
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeystrokeMgr.TestKeyUp
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeystrokeMgr::TestKeyUp


## -description




## -parameters




### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="https://msdn.microsoft.com/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>.


### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="https://msdn.microsoft.com/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>.


### -param pfEaten [out]

Pointer to a BOOL that indicates if the key event is handled. If this value receives <b>TRUE</b>, the key event is handled and the event should not be forwarded to the application. If this value is <b>FALSE</b>, the key event is not handled and the event should be forwarded to the application.


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



An application can determine if a key event is handled by the keystroke manager with this method. If this method is successful and <i>pfEaten</i> receives <b>TRUE</b>, the application should call <a href="https://msdn.microsoft.com/14415de3-f397-4866-b7d1-167c0931a80c">ITfKeystrokeMgr::KeyUp</a>. If this method does not return S_OK or <i>pfEaten</i> receives <b>FALSE</b>, the application should not call <b>ITfKeystrokeMgr::KeyUp</b> . The following is an example of how this is implemented.

<pre class="syntax" xml:space="preserve"><code>
if(msg.message == WM_KEYUP)
{
    if( pKeyboardMgr-&gt;TestKeyUp(msg.wParam, msg.lParam, &amp;fEaten) == S_OK 
        &amp;&amp; fEaten 
        &amp;&amp; pKeyboardMgr-&gt;KeyUp(msg.wParam, msg.lParam, &amp;fEaten) == S_OK 
        &amp;&amp; fEaten)
    {
        The key was handled by the keystroke manager or a text service. Do not pass the key to the application.
        continue;
    }
    else
    {
        //Let the application process the key. 
    }
}
</code></pre>
If the keystroke manager does not handle the key event, it passes the key event to the TSF text service by calling the TSF text service <a href="https://msdn.microsoft.com/2d105a20-3fb8-43aa-a36a-744803bd4035">ITfKeyEventSink::OnTestKeyUp</a> method.




## -see-also




<a href="https://msdn.microsoft.com/2d105a20-3fb8-43aa-a36a-744803bd4035">
        ITfKeyEventSink::OnTestKeyUp</a>



<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>



<a href="https://msdn.microsoft.com/14415de3-f397-4866-b7d1-167c0931a80c">
        ITfKeystrokeMgr::KeyUp</a>



<a href="https://msdn.microsoft.com/e1f03aff-ce6e-4bb6-ad08-666e04cf6c13">
        ITfKeystrokeMgr::TestKeyDown</a>



<a href="https://msdn.microsoft.com/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>
 

 

