---
UID: NF:msinkaut.IInkPicture.get_Renderer
title: IInkPicture::get_Renderer
author: windows-sdk-content
description: Gets or sets the InkRenderer object that is used to draw ink.
old-location: tablet\inkpicture_renderer.htm
tech.root: tablet
ms.assetid: 5df5918a-caca-4296-8464-3710ff904b10
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInkPicture interface [Tablet PC],Renderer property, IInkPicture.Renderer, IInkPicture.get_Renderer, IInkPicture::Renderer, IInkPicture::get_Renderer, IInkPicture::put_Renderer, InkPicture.get_Renderer, InkPicture.put_Renderer, Renderer property [Tablet PC], Renderer property [Tablet PC],IInkPicture interface, get_Renderer, msinkaut/IInkPicture::Renderer, msinkaut/IInkPicture::get_Renderer, msinkaut/IInkPicture::put_Renderer, put_Renderer, tablet.inkpicture_renderer
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IInkPicture.Renderer
 - IInkPicture.get_Renderer
 - IInkPicture.put_Renderer
 - InkPicture.get_Renderer
 - InkPicture.put_Renderer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkPicture::get_Renderer


## -description



Gets or sets the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object that is used to draw ink.



This property is read/write.


## -parameters


## -remarks



When handling certain window messages, changing the <b>Renderer</b> associated with the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> can cause a reentrant function call, generating unexpected results. For example, changing to a different <i>Renderer</i> or modifying its transforms within a message handler can result in a reentrant call. This affects the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). It is an issue with single-threaded apartment model applications.




## -see-also




<a href="https://msdn.microsoft.com/EA6AC3DD-5F13-442A-B93D-FF0A5333609A">IInkPicture</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>
 

 

