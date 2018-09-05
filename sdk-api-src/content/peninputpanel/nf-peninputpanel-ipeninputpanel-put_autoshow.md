---
UID: NF:peninputpanel.IPenInputPanel.put_AutoShow
title: IPenInputPanel::put_AutoShow
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets a value that indicates whether the pen input panel appears when focus is set on the attached control by using the pen.
old-location: tablet\peninputpanel_autoshow.htm
old-project: tablet
ms.assetid: c76533af-9b1d-413b-afa8-972ccfdce329
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: AutoShow property [Tablet PC], AutoShow property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],AutoShow property, IPenInputPanel.AutoShow, IPenInputPanel.put_AutoShow, IPenInputPanel::AutoShow, IPenInputPanel::get_AutoShow, IPenInputPanel::put_AutoShow, PenInputPanel.get_AutoShow, PenInputPanel.put_AutoShow, c76533af-9b1d-413b-afa8-972ccfdce329, get_AutoShow, peninputpanel/IPenInputPanel::AutoShow, peninputpanel/IPenInputPanel::get_AutoShow, peninputpanel/IPenInputPanel::put_AutoShow, put_AutoShow, tablet.peninputpanel_autoshow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: peninputpanel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EventMask
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.AutoShow
 - IPenInputPanel.get_AutoShow
 - IPenInputPanel.put_AutoShow
 - PenInputPanel.get_AutoShow
 - PenInputPanel.put_AutoShow
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: ADAM
---

# IPenInputPanel::put_AutoShow


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets or sets a value that indicates whether the pen input panel appears when focus is set on the attached control by using the pen.



This property is read/write.


## -parameters


## -remarks



When the <b>AutoShow</b> property is set to <b>VARIANT_FALSE</b>, Tablet PC Input Panel does not show until the <a href="https://msdn.microsoft.com/561b1a92-2e7e-4e8a-8fad-ebb515328cb7">Visible</a> property is set to <b>VARIANT_TRUE</b>. At this point, Tablet PC Input Panel is displayed but no hover target is shown.




## -see-also




<a href="https://msdn.microsoft.com/AA973F9D-264F-4D08-9D86-C5DAEF1C09D5">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

