---
UID: NF:msinkaut.IInkPicture.put_MousePointer
title: IInkPicture::put_MousePointer
author: windows-sdk-content
description: Gets or sets a value that indicates the type of mouse pointer that appears.
old-location: tablet\inkpicture_mousepointer.htm
old-project: tablet
ms.assetid: 94536770-01ef-41c5-9217-0aa2ef9c36ac
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IInkPicture interface [Tablet PC],MousePointer property, IInkPicture.MousePointer, IInkPicture.put_MousePointer, IInkPicture::MousePointer, IInkPicture::get_MousePointer, IInkPicture::put_MousePointer, InkPicture.get_MousePointer, InkPicture.put_MousePointer, MousePointer property [Tablet PC], MousePointer property [Tablet PC],IInkPicture interface, get_MousePointer, msinkaut/IInkPicture::MousePointer, msinkaut/IInkPicture::get_MousePointer, msinkaut/IInkPicture::put_MousePointer, put_MousePointer, tablet.inkpicture_mousepointer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkPicture.MousePointer
 - IInkPicture.get_MousePointer
 - IInkPicture.put_MousePointer
 - InkPicture.get_MousePointer
 - InkPicture.put_MousePointer
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkPicture::put_MousePointer


## -description



Gets or sets a value that indicates the type of mouse pointer that appears.



This property is read/write.


## -parameters


## -remarks



If you set the <b>MousePointer</b> property to <a href="https://msdn.microsoft.com/74f489f2-d568-4133-96e6-de15cbfabfe7">IMP_Default</a>, the mouse cursor setting is based on the current cursor's drawing attributes. If the ink collector is disabled, the mouse cursor setting is based on the underlying windows mouse cursor <a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes</a> property. If the <b>MousePointer</b> property is set to <b>IMP_Custom</b> and the <a href="https://msdn.microsoft.com/a095dca7-4dc9-4661-8c78-0e357a57f982">MouseIcon</a> property is <b>NULL</b>, then the ink collector no longer handles mouse cursor settings. Setting the mouse cursor to any other setting (other than the <b>MousePointer</b> property set to <b>IMP_Default</b> and the <b>MouseIcon</b> property set to <b>NULL</b>) forces the mouse cursor to use the current setting.

You can use this property when you want to indicate changes in functionality as the mouse pointer passes over controls on a form or dialog box. The <a href="https://msdn.microsoft.com/74f489f2-d568-4133-96e6-de15cbfabfe7">IMP_Hourglass</a> setting is useful for indicating that the user should wait for a process or operation to finish.




## -see-also




<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/74f489f2-d568-4133-96e6-de15cbfabfe7">InkMousePointer Enumeration</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>



<a href="https://msdn.microsoft.com/a095dca7-4dc9-4661-8c78-0e357a57f982">MouseIcon Property</a>
 

 

