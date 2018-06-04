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

# IWiaItem::DeviceDlg


## -description


The <b>IWiaItem::DeviceDlg</b> method is used by applications to display a dialog box to the user to prepare for image acquisition.


## -parameters




### -param hwndParent [in]

Type: <b>HWND</b>

Handle of the parent window of the dialog box.


### -param lFlags [in]

Type: <b>LONG</b>

Specifies a set of flags that control the dialog box's operation. Can be set to any of the following values:




<table class="clsStd">
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>Default behavior.</td>
</tr>
<tr>
<td>WIA_DEVICE_DIALOG_SINGLE_IMAGE</td>
<td>Restrict image selection to a single image in the device image acquisition dialog box.</td>
</tr>
<tr>
<td>WIA_DEVICE_DIALOG_USE_COMMON_UI</td>
<td>Use the system UI, if available, rather than the vendor-supplied UI. If the system UI is not available, the vendor UI is used. If neither UI is available, the function returns E_NOTIMPL.</td>
</tr>
</table>
 


### -param lIntent [in]

Type: <b>LONG</b>

Specifies what type of data the image is intended to represent. For a list of image intent values, see <a href="https://msdn.microsoft.com/171228d9-a619-49aa-964e-f72a7f294a9d">Image Intent Constants</a>.




<div class="alert"><b>Note</b>  This method ignores all WIA_INTENT_IMAGE_* image intents.</div>
<div> </div>

### -param plItemCount [out]

Type: <b>LONG*</b>

Receives the number of items in the array indicated by the <i>ppIWiaItem</i> parameter.


### -param ppIWiaItem [out]

Type: <b>IWiaItem***</b>

Receives the address of an array of pointers to <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interfaces. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition. For instance, this dialog box enables the user to select images to download from a camera. When using a scanner, it is also used to specify image scan properties such as brightness and contrast.

After this method returns, the application can use the <a href="https://msdn.microsoft.com/565e48b7-30c5-4c8b-ae4a-071c2e90b2f9">IWiaDataTransfer</a> interface to acquire the image.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method for each element in the array of interface pointers they receive through the <i>ppIWiaItem</i> parameter. Applications must also free the array using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.

It is recommended that applications make device and image selection available through a menu item named <b>From scanner or camera</b> on the <b>File</b> menu.



