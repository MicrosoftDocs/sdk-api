---
UID: NF:wmp.IWMPEvents.ScriptCommand
title: IWMPEvents::ScriptCommand (wmp.h)
description: The ScriptCommand event occurs when a synchronized command or URL is received.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","ScriptCommand method","IWMPEvents.ScriptCommand","IWMPEvents::ScriptCommand","IWMPEventsScriptCommand","ScriptCommand","ScriptCommand method [Windows Media Player]","ScriptCommand method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__scriptcommand","wmp/IWMPEvents::ScriptCommand"]
old-location: wmp\iwmpevents_iwmpevents__scriptcommand.htm
tech.root: WMP
ms.assetid: 1010961f-6d06-455a-9c14-bc06702e9e89
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],ScriptCommand method, IWMPEvents.ScriptCommand, IWMPEvents::ScriptCommand, IWMPEventsScriptCommand, ScriptCommand, ScriptCommand method [Windows Media Player], ScriptCommand method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__scriptcommand, wmp/IWMPEvents::ScriptCommand
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents::ScriptCommand
 - wmp/IWMPEvents::ScriptCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.ScriptCommand
---

# IWMPEvents::ScriptCommand


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ScriptCommand</b> event occurs when a synchronized command or URL is received.

## -parameters

### -param scType [in]

Specifies the type of script command.

### -param Param [in]

Specifies the script command.

## -remarks

Commands can be embedded along with the audio, video, or other data within a Windows Media file. The commands are comprised of a pair of Unicode strings associated with a designated time in the stream.

When playback reaches the time associated with the command, the Windows Media Player control sends a <b>ScriptCommand</b> event with two parameters. One parameter specifies the type of command being sent. The other parameter specifies the command. The type of parameter is used to determine how the command parameter is processed. Any type of command can be embedded in a Windows Media file to be handled by the <b>ScriptCommand</b> event.

The following table lists script command types that are processed automatically by Windows Media Player.

<table>
<tr>
<th>Type
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>CAPTION</td>
<td>The control displays the associated text in the DIV specified by <b>IWMPClosedCaption::get_captioningID</b>.</td>
</tr>
<tr>
<td>EVENT</td>
<td>Tells the control to execute instructions defined for the specified event.</td>
</tr>
<tr>
<td>FILENAME</td>
<td>The control resets its <b>URL</b> property, attempts to open the specified file, and begins playing the new stream immediately.</td>
</tr>
<tr>
<td>OPENEVENT</td>
<td>Buffers the associated EVENT command for timely execution of the EVENT script.</td>
</tr>
<tr>
<td>SYNCHRONIZEDLYRICLYRIC</td>
<td>The <i>Param</i> parameter contains the synchronized lyric text. Windows Media Player displays the lyric text in the closed caption area of the <b>Now Playing</b> feature.</td>
</tr>
<tr>
<td>TEXT</td>
<td>The control displays the associated text in the DIV specified by <b>IWMPClosedCaption::get_captioningID</b>.</td>
</tr>
<tr>
<td>URL</td>
<td>The control automatically opens the URL specified using the default Internet browser if the <b>IWMPSettings::put_invokeURLs</b> method has been called.</td>
</tr>
</table>
 

You can embed any other type of command as long as you provide reciprocal code to handle the command. Unknown commands are ignored by the Windows Media Player control, but they are still handed off to the <b>ScriptCommand</b> event.

The <b>ScriptCommand</b> event is not called if the file is being scanned in fast forward or fast reversed mode.

The value of event parameters is specified by Windows Media Player. It can be accessed or passed to a method in an imported JScript file by using the parameter name. This parameter name must be typed exactly as shown, including capitalization.

URL commands received by the Windows Media Player control are invoked automatically in the user's default Web browser if the <b>IWMPSettings::put_baseURL</b> method has been called. You can use the <b>IWMPSettings::put_defaultFrame</b> property to specify the target frame in which the webpage appears.

The URL sent to Windows Media Player is processed relative to the base URL specified by the <b>IWMPSettings::get_invokeURLs</b> method. The base URL is concatenated with the relatively specified URL, resulting in a fully specified URL that is passed as the command parameter by the <b>ScriptCommand</b> event.

The Windows Media Player control always processes incoming URL commands in the following manner:

<ol>
<li>A URL command is received.</li>
<li><b>IWMPSettings::put_baseURL</b> is used to create a full URL from the relative URL specified in the script command.</li>
<li><b>ScriptCommand</b> is called.</li>
<li>After <b>ScriptCommand</b> returns, <b>IWMPSettings::get_invokeURLs</b> is checked.</li>
<li>If <b>IWMPSettings::get_invokeURLs</b> is true and the command is a URL command, the specified URL is invoked. If <b>IWMPSettings::get_invokeURLs</b> is false or the command is not a URL command, the command is ignored.</li>
</ol>
When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersand (&amp;) characters and the name of the frame in the parameter field. The following example specifies that the URL http://myweb/mypage.html must be launched in the frame called myframe.


```cpp

scType = "URL"
Param = http://myweb/mypage.html&&myframe


```

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_captioningid">IWMPClosedCaption::get_captioningId</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_invokeurls">IWMPSettings::get_invokeURLs</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_baseurl">IWMPSettings::put_baseURL</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_defaultframe">IWMPSettings::put_defaultFrame</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_invokeurls">IWMPSettings::put_invokeURLs</a>