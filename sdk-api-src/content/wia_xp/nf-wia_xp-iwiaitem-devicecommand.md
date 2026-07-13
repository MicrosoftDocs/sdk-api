---
UID: NF:wia_xp.IWiaItem.DeviceCommand
title: IWiaItem::DeviceCommand (wia_xp.h)
description: The IWiaItem::DeviceCommand issues a command to a Windows Image Acquisition (WIA) hardware device.
helpviewer_keywords: ["DeviceCommand","DeviceCommand method [WIA]","DeviceCommand method [WIA]","IWiaItem interface","IWiaItem interface [WIA]","DeviceCommand method","IWiaItem.DeviceCommand","IWiaItem::DeviceCommand","_wia_IWiaItem_DeviceCommand","wia._wia_IWiaItem_DeviceCommand","wia_xp/IWiaItem::DeviceCommand"]
old-location: wia\_wia_IWiaItem_DeviceCommand.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\devicecommand.htm
ms.date: 12/05/2018
ms.keywords: DeviceCommand, DeviceCommand method [WIA], DeviceCommand method [WIA],IWiaItem interface, IWiaItem interface [WIA],DeviceCommand method, IWiaItem.DeviceCommand, IWiaItem::DeviceCommand, _wia_IWiaItem_DeviceCommand, wia._wia_IWiaItem_DeviceCommand, wia_xp/IWiaItem::DeviceCommand
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
 - IWiaItem::DeviceCommand
 - wia_xp/IWiaItem::DeviceCommand
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
 - IWiaItem.DeviceCommand
archived: true
---

# IWiaItem::DeviceCommand


## -description

The <b>IWiaItem::DeviceCommand</b> issues a command to a Windows Image Acquisition (WIA) hardware device.

## -parameters

### -param lFlags [in]

Type: <b>LONG</b>

Currently unused. Should be set to zero.

### -param pCmdGUID [in]

Type: <b>const GUID*</b>

Specifies a unique identifier that specifies the command to send to the WIA hardware device. For a list of valid device commands, see <a href="/windows/desktop/wia/-wia-wia-device-commands">WIA Device Commands</a>.

### -param pIWiaItem [in, out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a>**</b>

On output, this pointer points to the item created by the command, if any.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications use this method to send WIA commands to hardware devices. 

When the application sends the WIA_CMD_TAKE_PICTURE command to the device, <b>IWiaItem::DeviceCommand</b>, the WIA run-time system creates the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> object to represent the image. The <b>IWiaItem::DeviceCommand</b> method stores the address of the interface in the <i>pIWiaItem</i>  parameter. 

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>pIWiaItem</i> parameter.