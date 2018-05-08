---
UID: NF:uiribbon.IUIImageFromBitmap.CreateImage
title: IUIImageFromBitmap::CreateImage
author: windows-driver-content
description: Creates an IUIImage object from a bitmap image.
old-location: windowsribbon\windowsribbon_iuiimagefrombitmap_createimage.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiimagefrombitmap\createimage.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CreateImage, CreateImage method [Windows Ribbon], CreateImage method [Windows Ribbon],IUIImageFromBitmap interface, IUIImageFromBitmap interface [Windows Ribbon],CreateImage method, IUIImageFromBitmap.CreateImage, IUIImageFromBitmap::CreateImage, scenicintent_IUIImageFromBitmap_CreateImage, uiribbon/IUIImageFromBitmap::CreateImage, windowsribbon.windowsribbon_iuiimagefrombitmap_createimage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UI_VIEWVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mshtml.dll
api_name:
-	IUIImageFromBitmap.CreateImage
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUIImageFromBitmap::CreateImage


## -description


Creates an <a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a> object from a bitmap image.


## -parameters




### -param bitmap [in]

Type: <b>HBITMAP</b>


					A handle to the bitmap that contains the image.
				


### -param options [in]

Type: <b><a href="https://msdn.microsoft.com/0feb95ce-1ec9-4ff0-81f2-921e5ae57065">UI_OWNERSHIP</a></b>


					The <a href="https://msdn.microsoft.com/0feb95ce-1ec9-4ff0-81f2-921e5ae57065">ownership conditions</a> under which 
					an image is created.
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>UI_OWNERSHIP_TRANSFER</td>
<td>
					If <b>UI_OWNERSHIP_TRANSFER</b> is specified as the value of 
				<i>options</i>, then the Ribbon framework owns 
					the handle to the bitmap (HBITMAP) through the <a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a> object and 
					releases it when the framework no longer requires it.
				<div class="alert"><b>Note</b>  
					This option prevents the Ribbon host application from safely referencing the same HBITMAP 
					elsewhere in the application UI.
				</div>
<div> </div>
</td>
</tr>
<tr>
<td>UI_OWNERSHIP_COPY</td>
<td>
					If <b>UI_OWNERSHIP_COPY</b> is specified as the value of 
				<i>options</i>, then the host application owns the 
					HBITMAP and is able to reference the same HBITMAP for use elsewhere in the 
					UI.
				<div class="alert"><b>Note</b>  
					This option places responsibility for releasing the HBITMAP on the 
					host application.
				</div>
<div> </div>
</td>
</tr>
</table>
 


### -param image [out]

Type: <b><a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a>**</b>


					When this method returns, contains the address of a pointer variable that receives the <a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a> object. 
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




				 This factory method is useful when an application dynamically generates an image 
				 resource and wants to pass the new HBITMAP to the Ribbon, 
				 for example, loading a Portable Network Graphics (PNG) through the Windows Imaging Component (WIC) or using 
				 <a href="http://go.microsoft.com/fwlink/p/?linkid=133010">CreateDIBSection</a> to create an image for a new style 
				 in a styles gallery.
			


				This method is also useful for applications that require a 
				pre-existing bitmap image that has not been rendered obsolete by the Ribbon, 
				for example, a legacy toolbar image strip.
			


				Specify <b>UI_OWNERSHIP_COPY</b> as the value for <i>options</i> if the Ribbon is being implemented in an 
				existing application and minimal code changes are required. This method uses extra memory 
				for the additional image.
			


				Specify <b>UI_OWNERSHIP_TRANSFER</b> as the value for <i>options</i> to minimize memory usage.
			




## -see-also




<a href="https://msdn.microsoft.com/f2b98d96-895e-40aa-9969-98bf1c0c8e5f">IUIImageFromBitmap</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

