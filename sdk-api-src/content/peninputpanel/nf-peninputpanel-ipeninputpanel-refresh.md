---
UID: NF:peninputpanel.IPenInputPanel.Refresh
title: IPenInputPanel::Refresh
author: windows-sdk-content
description: Refresh is no longer available for use as of Windows XP Tablet PC Edition.
old-location: tablet\peninputpanel_refresh.htm
tech.root: tablet
ms.assetid: 7f135184-76cc-4636-8c20-db29ca7d5540
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 7f135184-76cc-4636-8c20-db29ca7d5540, IPenInputPanel interface [Tablet PC],Refresh method, IPenInputPanel.Refresh, IPenInputPanel::Refresh, Refresh, Refresh method [Tablet PC], Refresh method [Tablet PC],IPenInputPanel interface, peninputpanel/IPenInputPanel::Refresh, tablet.peninputpanel_refresh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPenInputPanel::Refresh


## -description


<p class="CCE_Message">[<b>Refresh</b> is no longer available for use as of Windows XP Tablet PC Edition. Instead, use <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.]

Updates and restores the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> properties based on Tablet PC Input Panel settings, automatically positions the pen input panel, and sets the user interface to the default panel.


## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.
              

</td>
</tr>
</table>
 




## -remarks



The <b>Refresh</b> method restores the default panel. For example, if the <a href="https://msdn.microsoft.com/2b0ff320-02ce-4b23-ae47-91504c93ac24">DefaultPanel</a> property is set to <a href="https://msdn.microsoft.com/fbf0ecce-0286-4d1b-99ba-9d28fc25da30">Keyboard</a> and the <a href="https://msdn.microsoft.com/536ba874-b9f9-45c9-bf9a-a64679afc861">CurrentPanel</a> property is set to <b>Handwriting</b>, the <b>Refresh</b> method sets the pen input panel to <b>Keyboard</b>. If the <b>DefaultPanel</b> property is set to <b>Default</b>, the <b>Refresh</b> method does not change the pen input panel.

The <b>Refresh</b> method automatically positions the pen input panel relative to the control to which it is attached.

The <b>Refresh</b> method updates the pen input panel using the Input Panel settings. For instance, you can make changes to the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, and then call <b>Refresh</b> to restore the settings to those copied from the Input Panel.

The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object is updated automatically whenever the Input Panel settings change.

Calling <b>Refresh</b> while the pen input panel does not have focus will generate an error.

<div class="alert"><b>Note</b>  Normally, you won't need to call <b>Refresh</b> because all of the above is executed during activation of the pen input panel. However, if the <a href="https://msdn.microsoft.com/c76533af-9b1d-413b-afa8-972ccfdce329">AutoShow</a> property is set to <b>FALSE</b>, you can disable activation of the pen input panel. Therefore, the <b>Refresh</b> method is needed.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/AA973F9D-264F-4D08-9D86-C5DAEF1C09D5">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

