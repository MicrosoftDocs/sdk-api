---
UID: NF:wia_xp.IWiaDevMgr.SelectDeviceDlg
title: IWiaDevMgr::SelectDeviceDlg (wia_xp.h)
description: The IWiaDevMgr::SelectDeviceDlg displays a dialog box that enables the user to select a hardware device for image acquisition.
helpviewer_keywords: ["IWiaDevMgr interface [WIA]","SelectDeviceDlg method","IWiaDevMgr.SelectDeviceDlg","IWiaDevMgr::SelectDeviceDlg","SelectDeviceDlg","SelectDeviceDlg method [WIA]","SelectDeviceDlg method [WIA]","IWiaDevMgr interface","_wia_IWiaDevMgr_SelectDeviceDlg","wia._wia_IWiaDevMgr_SelectDeviceDlg","wia_xp/IWiaDevMgr::SelectDeviceDlg"]
old-location: wia\_wia_IWiaDevMgr_SelectDeviceDlg.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\selectdevicedlg.htm
ms.date: 12/05/2018
ms.keywords: IWiaDevMgr interface [WIA],SelectDeviceDlg method, IWiaDevMgr.SelectDeviceDlg, IWiaDevMgr::SelectDeviceDlg, SelectDeviceDlg, SelectDeviceDlg method [WIA], SelectDeviceDlg method [WIA],IWiaDevMgr interface, _wia_IWiaDevMgr_SelectDeviceDlg, wia._wia_IWiaDevMgr_SelectDeviceDlg, wia_xp/IWiaDevMgr::SelectDeviceDlg
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
 - IWiaDevMgr::SelectDeviceDlg
 - wia_xp/IWiaDevMgr::SelectDeviceDlg
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
 - IWiaDevMgr.SelectDeviceDlg
archived: true
---

# IWiaDevMgr::SelectDeviceDlg


## -description

The <b>IWiaDevMgr::SelectDeviceDlg</b> displays a dialog box that enables the user to select a hardware device for image acquisition.

## -parameters

### -param hwndParent [in]

Type: <b>HWND</b>

Handle of the window that owns the <b>Select Device</b> dialog box.

### -param lDeviceType [in]

Type: <b>LONG</b>

Specifies which type of WIA device to use. Can be set to <b>StiDeviceTypeDefault</b>, <b>StiDeviceTypeScanner</b>, or <b>StiDeviceTypeDigitalCamera</b>.

### -param lFlags [in]

Type: <b>LONG</b>

Specifies dialog box behavior. Can be set to any of the following values:



<table class="clsStd">
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>Use the default behavior.</td>
</tr>
<tr>
<td>WIA_SELECT_DEVICE_NODEFAULT</td>
<td>Display the dialog box even if there is only one matching device. For more information, see the <b>Remarks</b> section of this reference page.</td>
</tr>
</table>

### -param pbstrDeviceID [in, out]

Type: <b>BSTR*</b>

On output, receives a string which contains the device's identifier string. On input, pass the address of a pointer if this information is needed, or <b>NULL</b> if it is not needed.

### -param ppItemRoot [out, retval]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a>**</b>

Receives the address of a pointer to the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> interface of the root item of the tree that represents the selected WIA device. If no devices are found, it contains the value <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

This method returns the following values:

<table class="clsStd">
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>A device was successfully selected.</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>The user canceled the dialog box.</td>
</tr>
<tr>
<td>WIA_S_NO_DEVICE_AVAILABLE</td>
<td>There are no WIA hardware devices that match the specifications given in the <i>lDeviceType</i> parameter.</td>
</tr>
</table>

## -remarks

This method creates and displays the <b>Select Device</b> dialog box so the user can select a WIA device for image acquisition. If a device is successfully selected, the <b>IWiaDevMgr::SelectDeviceDlg</b> method creates a hierarchical tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects for the device. It stores a pointer to the <b>IWiaItem</b> interface of the root item in the parameter <i>ppItemRoot</i>.

Particular types of devices may be displayed to the user by specifying the device types through the <i>lDeviceType</i> parameter. If only one device meets the specification, <b>IWiaDevMgr::SelectDeviceDlg</b> does not display the <b>Select Device</b> dialog box. Instead it creates the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> tree for the device and store a pointer to the  <b>IWiaItem</b> interface of the root item in the parameter <i>ppItemRoot</i>. You can override this behavior and force <b>IWiaDevMgr::SelectDeviceDlg</b> to display the <b>Select Device</b> dialog box by passing WIA_SELECT_DEVICE_NODEFAULT as the value for the <i>lFlags</i> parameter.

If more than one WIA device matches the specification, all matching devices are displayed in the <b>Select Device</b> dialog box so the user may choose one.

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppItemRoot</i> parameter.

It is recommended that applications make device and image selection available through a menu item named <b>From scanner or camera</b> on the <b>File</b> menu.