---
UID: NF:wia_xp.IWiaItem.DeviceDlg
title: IWiaItem::DeviceDlg (wia_xp.h)
description: The IWiaItem::DeviceDlg method is used by applications to display a dialog box to the user to prepare for image acquisition.
helpviewer_keywords: ["DeviceDlg","DeviceDlg method [WIA]","DeviceDlg method [WIA]","IWiaItem interface","IWiaItem interface [WIA]","DeviceDlg method","IWiaItem.DeviceDlg","IWiaItem::DeviceDlg","_wia_IWiaItem_DeviceDlg","wia._wia_IWiaItem_DeviceDlg","wia_xp/IWiaItem::DeviceDlg"]
old-location: wia\_wia_IWiaItem_DeviceDlg.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\devicedlg.htm
ms.date: 12/05/2018
ms.keywords: DeviceDlg, DeviceDlg method [WIA], DeviceDlg method [WIA],IWiaItem interface, IWiaItem interface [WIA],DeviceDlg method, IWiaItem.DeviceDlg, IWiaItem::DeviceDlg, _wia_IWiaItem_DeviceDlg, wia._wia_IWiaItem_DeviceDlg, wia_xp/IWiaItem::DeviceDlg
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaItem::DeviceDlg
 - wia_xp/IWiaItem::DeviceDlg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItem.DeviceDlg
archived: true
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

Specifies what type of data the image is intended to represent. For a list of image intent values, see <a href="/windows/desktop/wia/-wia-imageintentconstants">Image Intent Constants</a>.




<div class="alert"><b>Note</b>  This method ignores all WIA_INTENT_IMAGE_* image intents.</div>
<div> </div>

### -param plItemCount [out]

Type: <b>LONG*</b>

Receives the number of items in the array indicated by the <i>ppIWiaItem</i> parameter.

### -param ppIWiaItem [out]

Type: <b>IWiaItem***</b>

Receives the address of an array of pointers to <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> interfaces.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition. For instance, this dialog box enables the user to select images to download from a camera. When using a scanner, it is also used to specify image scan properties such as brightness and contrast.

After this method returns, the application can use the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer">IWiaDataTransfer</a> interface to acquire the image.

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each element in the array of interface pointers they receive through the <i>ppIWiaItem</i> parameter. Applications must also free the array using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

It is recommended that applications make device and image selection available through a menu item named <b>From scanner or camera</b> on the <b>File</b> menu.