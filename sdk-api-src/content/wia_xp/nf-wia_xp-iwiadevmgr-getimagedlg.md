---
UID: NF:wia_xp.IWiaDevMgr.GetImageDlg
title: IWiaDevMgr::GetImageDlg (wia_xp.h)
description: The IWiaDevMgr::GetImageDlg method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) device and write the image to a specified file.
helpviewer_keywords: ["GetImageDlg","GetImageDlg method [WIA]","GetImageDlg method [WIA]","IWiaDevMgr interface","IWiaDevMgr interface [WIA]","GetImageDlg method","IWiaDevMgr.GetImageDlg","IWiaDevMgr::GetImageDlg","_wia_IWiaDevMgr_GetImageDlg","wia._wia_IWiaDevMgr_GetImageDlg","wia_xp/IWiaDevMgr::GetImageDlg"]
old-location: wia\_wia_IWiaDevMgr_GetImageDlg.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\getimagedlg.htm
ms.date: 12/05/2018
ms.keywords: GetImageDlg, GetImageDlg method [WIA], GetImageDlg method [WIA],IWiaDevMgr interface, IWiaDevMgr interface [WIA],GetImageDlg method, IWiaDevMgr.GetImageDlg, IWiaDevMgr::GetImageDlg, _wia_IWiaDevMgr_GetImageDlg, wia._wia_IWiaDevMgr_GetImageDlg, wia_xp/IWiaDevMgr::GetImageDlg
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
 - IWiaDevMgr::GetImageDlg
 - wia_xp/IWiaDevMgr::GetImageDlg
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
 - IWiaDevMgr.GetImageDlg
archived: true
---

# IWiaDevMgr::GetImageDlg


## -description

The <b>IWiaDevMgr::GetImageDlg</b> method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) device and write the image to a specified file. This method combines the functionality of <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg">IWiaDevMgr::SelectDeviceDlg</a> to completely encapsulate image acquisition within a single API call.

## -parameters

### -param hwndParent [in]

Type: <b>HWND</b>

Handle of the window that owns the <b>Get Image</b> dialog box.

### -param lDeviceType [in]

Type: <b>LONG</b>

Specifies which type of WIA device to use. Is set to <b>StiDeviceTypeDefault</b>, <b>StiDeviceTypeScanner</b>, or <b>StiDeviceTypeDigitalCamera</b>.

### -param lFlags [in]

Type: <b>LONG</b>

Specifies dialog box behavior. Can be set to the following values:



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
<td>WIA_SELECT_DEVICE_NODEFAULT</td>
<td>Force this method to display the <b>Select Device</b> dialog box. For more information, see the <b>Remarks</b> section of this reference page.</td>
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

### -param pItemRoot [in]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a>*</b>

Pointer to the interface of the hierarchical tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects returned by <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice">IWiaDevMgr::CreateDevice</a>.

### -param bstrFilename [in]

Type: <b>BSTR</b>

Specifies the name of the file to which the image data is written.

### -param pguidFormat [in, out]

Type: <b>GUID*</b>

On input, contains a pointer to a GUID that specifies the format to use. On output, holds the format used. Pass IID_NULL to use the default format.

## -returns

Type: <b>HRESULT</b>

<b>IWiaDevMgr::GetImageDlg</b> returns S_FALSE if the user cancels the device selection or image acquisition dialog boxes, WIA_S_NO_DEVICE_AVAILABLE if no WIA device is currently available, E_NOTIMPL if no UI is available, and S_OK if the data is transferred successfully.

<b>IWiaDevMgr::GetImageDlg</b> returns a value specified in <a href="/windows/desktop/wia/-wia-error-codes">Error Codes</a>, or a standard COM error if it fails for any reason other than those specified.

## -remarks

Invoking this method displays a dialog box that enables users to acquire images. It can also display the <b>Select Device</b> dialog box created by the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg">IWiaDevMgr::SelectDeviceDlg</a> method. 

If the application passes <b>NULL</b> for the value of the <i>pItemRoot</i> parameter, <b>IWiaDevMgr::GetImageDlg</b> displays the <b>Select Device</b> dialog box that lets the user select the WIA input device. If the application specifies a WIA input device by passing a pointer to the device's item tree through the <i>pItemRoot</i> parameter, <b>IWiaDevMgr::GetImageDlg</b> does not display the <b>Select Device</b> dialog box. Instead, it will use the specified input device to acquire the image.

When using the <b>Select Device</b> dialog box, applications can specify types of WIA input devices. To do so, they must set the <i>pItemRoot</i> parameter to <b>NULL</b> and pass the appropriate constants through the <i>lDeviceType</i> parameter. If more than one device of the specified type is present, the <b>IWiaDevMgr::GetImageDlg</b> displays the <b>Select Device</b> dialog box to let the user select which device will be used. 

If <b>IWiaDevMgr::GetImageDlg</b> finds only one matching device, it will not display the <b>Select Device</b> dialog box. Instead, it will select the matching device. You can override this behavior and force <b>IWiaDevMgr::GetImageDlg</b> to display the <b>Select Device</b> dialog box by passing WIA_SELECT_DEVICE_NODEFAULT as the value for the <i>lFlags</i> parameter.

It is recommended that applications make device and image selection available through a menu item named <b>From scanner or camera</b> on the <b>File</b> menu.

The dialog must have sufficient rights to the folder for <i>bstrFilename</i> that it can save the file with a unique file name. The folder should also be protected with an access control list (ACL) because it contains user data.