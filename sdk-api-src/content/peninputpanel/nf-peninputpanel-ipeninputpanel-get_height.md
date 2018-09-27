---
UID: NF:peninputpanel.IPenInputPanel.get_Height
title: IPenInputPanel::get_Height
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the height of the pen input panel in client coordinates.
old-location: tablet\peninputpanel_height.htm
tech.root: tablet
ms.assetid: 5815f184-1ae4-4617-9aa6-acf727aff202
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 5815f184-1ae4-4617-9aa6-acf727aff202, Height property [Tablet PC], Height property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],Height property, IPenInputPanel.Height, IPenInputPanel.get_Height, IPenInputPanel::Height, IPenInputPanel::get_Height, PenInputPanel.get_Height, get_Height, peninputpanel/IPenInputPanel::Height, peninputpanel/IPenInputPanel::get_Height, tablet.peninputpanel_height
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
 - IPenInputPanel.Height
 - IPenInputPanel.get_Height
 - PenInputPanel.get_Height
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPenInputPanel::get_Height


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets the height of the pen input panel in client coordinates.



This property is read-only.


## -parameters


## -remarks



The height of the pen input panel is dependent on the screen resolution for the particular Tablet PC. The panel height is the number of pixels equal to 1.25 inches. The default value at 96 dots per inch (dpi) is 157 pixels. The default value at 120 dpi is 196 pixels. The default value at 133 dpi is 218 pixels.

Starting with Microsoft Windows XP Tablet PC Edition 2005, the Tablet PC Input Panel allows the user to continue entering handwriting by automatically increasing the size of the Tablet PC Input Panel to accommodate new handwriting. The <b>Height</b> and <a href="https://msdn.microsoft.com/81173c64-5d8b-48ae-866c-5292814a97c0">Width</a> properties do not update to reflect the new size as the Tablet PC Input Panel grows. These properties return the original size of the Tablet PC Input Panel. They also do not report the dimensions of the Tablet PC Input Panel hover target.




## -see-also




<a href="https://msdn.microsoft.com/AA973F9D-264F-4D08-9D86-C5DAEF1C09D5">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>



<a href="https://msdn.microsoft.com/81173c64-5d8b-48ae-866c-5292814a97c0">Width Property [PenInputPanel Class]</a>
 

 

