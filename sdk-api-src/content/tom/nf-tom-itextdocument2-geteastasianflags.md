---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITextDocument2::GetEastAsianFlags


## -description


Gets the East Asian flags.


## -parameters




### -param pFlags [out, retval]

Type: <b>long*</b>

The East Asian flags. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomRE10Mode"></a><a id="tomre10mode"></a><a id="TOMRE10MODE"></a><dl>
<dt><b>tomRE10Mode</b></dt>
</dl>
</td>
<td width="60%">
TOM version 1.0 emulation mode.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUseAtFont"></a><a id="tomuseatfont"></a><a id="TOMUSEATFONT"></a><dl>
<dt><b>tomUseAtFont</b></dt>
</dl>
</td>
<td width="60%">
Use @ fonts for CJK vertical text.

</td>
</tr>
<tr>
<td width="40%"><a id="tomTextFlowMask"></a><a id="tomtextflowmask"></a><a id="TOMTEXTFLOWMASK"></a><dl>
<dt><b>tomTextFlowMask</b></dt>
</dl>
</td>
<td width="60%">
A mask for the following four text orientations:

<dl>
<dt><b>tomTextFlowES</b></dt>
<dd>
Ordinary left-to-right horizontal text.

</dd>
<dt><b>tomTextFlowSW</b></dt>
<dd>
Ordinary East Asian vertical text.

</dd>
<dt><b>tomTextFlowWN</b></dt>
<dd>
An alternative orientation.

</dd>
<dt><b>tomTextFlowNE</b></dt>
<dd>
An alternative orientation.

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="tomUsePassword"></a><a id="tomusepassword"></a><a id="TOMUSEPASSWORD"></a><dl>
<dt><b>tomUsePassword</b></dt>
</dl>
</td>
<td width="60%">
Use password control.

</td>
</tr>
<tr>
<td width="40%"><a id="tomNoIME"></a><a id="tomnoime"></a><a id="TOMNOIME"></a><dl>
<dt><b>tomNoIME</b></dt>
</dl>
</td>
<td width="60%">
Turn off IME operation (see <a href="Rich_Edit_Control_Styles.htm">ES_NOIME</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="tomSelfIME"></a><a id="tomselfime"></a><a id="TOMSELFIME"></a><dl>
<dt><b>tomSelfIME</b></dt>
</dl>
</td>
<td width="60%">
The rich edit host handles IME operation (see <a href="Rich_Edit_Control_Styles.htm">ES_SELFIME</a>) .

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

