---
UID: NS:winuser.tagSERIALKEYSW
title: tagSERIALKEYSW
author: windows-sdk-content
description: Contains information about the SerialKeys accessibility feature, which interprets data from a communication aid attached to a serial port as commands causing the system to simulate keyboard and mouse input.
old-location: winauto\serialkeys.htm
old-project: WinAuto
ms.assetid: 934446ab-b6bc-49f9-ab26-34eb3dc88f05
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: "*LPSERIALKEYSW, LPSERIALKEYS, LPSERIALKEYS structure pointer [Windows Accessibility], SERIALKEYS, SERIALKEYS structure [Windows Accessibility], SERIALKEYSW, SERKF_AVAILABLE, SERKF_INDICATOR, SERKF_SERIALKEYSON, _win32_SERIALKEYS_str, msaa.serialkeys, tagSERIALKEYSA, tagSERIALKEYSW, winauto.serialkeys, winuser/LPSERIALKEYS, winuser/SERIALKEYS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: SERIALKEYSW, *LPSERIALKEYSW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - SERIALKEYS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagSERIALKEYSW structure


## -description



        Contains information about the SerialKeys accessibility feature, which interprets data from a communication aid attached to a serial port as commands causing the system to simulate keyboard and mouse input.
      


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the structure size, in bytes.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


Specifies a combination of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERKF_AVAILABLE"></a><a id="serkf_available"></a><dl>
<dt><b>SERKF_AVAILABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The SerialKeys feature is available.

</td>
</tr>
<tr>
<td width="40%"><a id="SERKF_INDICATOR"></a><a id="serkf_indicator"></a><dl>
<dt><b>SERKF_INDICATOR</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
A visual indicator is displayed when the SerialKeys feature is on. This value is not currently used and is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SERKF_SERIALKEYSON"></a><a id="serkf_serialkeyson"></a><dl>
<dt><b>SERKF_SERIALKEYSON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The SerialKeys feature is on.

</td>
</tr>
</table>
 


### -field lpszActivePort

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

Points to a string that contains the name of the serial port that receives input from the communication aid when the SerialKeys feature is on. If no port is being used, this member is <b>NULL</b>. If this member is "Auto", the system watches all unused serial ports for input from communication aids.


### -field lpszPort

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

Reserved; must be <b>NULL</b>.


### -field iBaudRate

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the baud rate setting for the serial port specified by the <b>lpszActivePort</b> member. This member should be set to one of the CBR_ values defined in the winbase.h header file. If <b>lpszActivePort</b> is <b>NULL</b>, this member is zero.


### -field iPortState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


Specifies the state of the port specified by the <b>lpszActivePort</b> member. If <b>lpszActivePort</b> is <b>NULL</b>, <b>iPortState</b> is zero; otherwise, it is one of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
All input on this port is ignored by the SerialKeys feature.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Input on this port is watched for SerialKeys activation sequences when no other application has the port open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
All input on this port is treated as SerialKeys commands.

</td>
</tr>
</table>
 


### -field iActive

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the active port.


## -remarks



An application uses this structure when calling the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function with the <b>SPI_GETSERIALKEYS</b> or <b>SPI_SETSERIALKEYS</b> value. When using <b>SPI_GETSERIALKEYS</b>, an application must specify the <b>cbSize</b>, <b>lpszActivePort</b>, and <b>lpszPort</b> members of the <b>SERIALKEYS</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. An application must specify all structure members when using the <b>SPI_SETSERIALKEYS</b> value.




## -see-also




<a href="https://msdn.microsoft.com/0ff480ae-18e3-413d-b208-a67fbae28c25">Accessibility Structures</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

