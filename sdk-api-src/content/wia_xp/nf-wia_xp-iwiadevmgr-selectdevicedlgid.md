---
UID: NF:wia_xp.IWiaDevMgr.SelectDeviceDlgID
title: IWiaDevMgr::SelectDeviceDlgID (wia_xp.h)
description: The IWiaDevMgr::SelectDeviceDlgID method displays a dialog box that enables the user to select a hardware device for image acquisition.
helpviewer_keywords: ["IWiaDevMgr interface [WIA]","SelectDeviceDlgID method","IWiaDevMgr.SelectDeviceDlgID","IWiaDevMgr::SelectDeviceDlgID","SelectDeviceDlgID","SelectDeviceDlgID method [WIA]","SelectDeviceDlgID method [WIA]","IWiaDevMgr interface","_wia_IWiaDevMgr_SelectDeviceDlgID","wia._wia_IWiaDevMgr_SelectDeviceDlgID","wia_xp/IWiaDevMgr::SelectDeviceDlgID"]
old-location: wia\_wia_IWiaDevMgr_SelectDeviceDlgID.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\selectdevicedlgid.htm
ms.date: 12/05/2018
ms.keywords: IWiaDevMgr interface [WIA],SelectDeviceDlgID method, IWiaDevMgr.SelectDeviceDlgID, IWiaDevMgr::SelectDeviceDlgID, SelectDeviceDlgID, SelectDeviceDlgID method [WIA], SelectDeviceDlgID method [WIA],IWiaDevMgr interface, _wia_IWiaDevMgr_SelectDeviceDlgID, wia._wia_IWiaDevMgr_SelectDeviceDlgID, wia_xp/IWiaDevMgr::SelectDeviceDlgID
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
 - IWiaDevMgr::SelectDeviceDlgID
 - wia_xp/IWiaDevMgr::SelectDeviceDlgID
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
 - IWiaDevMgr.SelectDeviceDlgID
archived: true
---

# IWiaDevMgr::SelectDeviceDlgID


## -description

The <b>IWiaDevMgr::SelectDeviceDlgID</b> method displays a dialog box that enables the user to select a hardware device for image acquisition.

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

### -param pbstrDeviceID [out, retval]

Type: <b>BSTR*</b>

Pointer to a string that receives the identifier string of the device.

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
<td>There are no WIA hardware devices attached to the user's computer that match the specifications.</td>
</tr>
</table>

## -remarks

This method works in a similar manner to <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg">IWiaDevMgr::SelectDeviceDlg</a>. The primary difference is that if it finds a matching device, it does not create the hierarchical tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects for the device.

Like <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg">IWiaDevMgr::SelectDeviceDlg</a>, the <b>IWiaDevMgr::SelectDeviceDlgID</b> method creates and displays the <b>Select Device</b> dialog box. This enables the user to select a WIA device for image acquisition. If a device is successfully selected, the <b>IWiaDevMgr::SelectDeviceDlgID</b> method passes its identifier string to the application through its <i>pbstrDeviceID</i> parameter. 

Particular types of devices may be displayed to the user by specifying the device types through the <i>lDeviceType</i> parameter. If only one device meets the specification, <b>IWiaDevMgr::SelectDeviceDlgID</b> does not display the <b>Select Device</b> dialog box. Instead it passes the device's identifier string to the application without displaying the dialog box. You can override this behavior and force <b>IWiaDevMgr::SelectDeviceDlgID</b> to display the <b>Select Device</b> dialog box by passing WIA_SELECT_DEVICE_NODEFAULT as the value for the <i>lFlags</i> parameter.

If more than one WIA device matches the specification, all matching devices are displayed in the <b>Select Device</b> dialog box so the user may choose one.

It is recommended that applications make device and image selection available through a menu item named <b>From scanner or camera</b> on the <b>File</b> menu.