---
UID: NF:micaut.IMathInputControl.EnableExtendedButtons
title: IMathInputControl::EnableExtendedButtons
author: windows-sdk-content
description: Determines whether the extended set of control buttons is shown.
old-location: tablet\imathinputcontrol_enableextendedbuttons.htm
old-project: tablet
ms.assetid: e8cdae54-ff0b-4361-bd38-1b99137736ab
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: EnableExtendedButtons, EnableExtendedButtons method [Tablet PC], EnableExtendedButtons method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],EnableExtendedButtons method, IMathInputControl.EnableExtendedButtons, IMathInputControl::EnableExtendedButtons, micaut/IMathInputControl::EnableExtendedButtons, tablet.imathinputcontrol_enableextendedbuttons
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: micaut.h
req.include-header: Micaut.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Micaut.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.EnableExtendedButtons
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMathInputControl::EnableExtendedButtons


## -description


Determines whether the extended set of control buttons is shown.


## -parameters




### -param Extended [in]

<b>VARIANT_TRUE</b> to show the extended button set; <b>VARIANT_FALSE</b> to show the basic button set.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The basic button set is shown by default.

The basic button set contains the <b>Clear</b>, <b>Erase</b>, <b>Insert</b>, <b>Select and Correct</b>, and <b>Write</b> buttons. The extended button set contains the basic set plus the <b>Redo</b> and <b>Undo</b> buttons.

The following image shows the Math Input Control with extended buttons enabled.



<img alt="Math input control with extended buttons enabled" src="./images/MIC.png"/>
The following image shows the Math Input Control with extended buttons disabled.



<img alt="Math input control with extended buttons disabled" src="./images/MIC_no_extended.png"/>

#### Examples

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    hr = g_spMIC-&gt;EnableExtendedButtons(VARIANT_TRUE);
  </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/922562be-4d5b-45b6-ad0b-49176f893c8e">Customizing the Math Input Control</a>



<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

