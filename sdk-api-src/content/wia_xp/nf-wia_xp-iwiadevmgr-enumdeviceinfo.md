---
UID: NF:wia_xp.IWiaDevMgr.EnumDeviceInfo
title: IWiaDevMgr::EnumDeviceInfo
author: windows-sdk-content
description: Applications use the IWiaDevMgr::EnumDeviceInfo method to enumerate property information for each available Windows Image Acquisition (WIA) device.
old-location: wia\_wia_IWiaDevMgr_EnumDeviceInfo.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\enumdeviceinfo.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumDeviceInfo, EnumDeviceInfo method [WIA], EnumDeviceInfo method [WIA],IWiaDevMgr interface, IWiaDevMgr interface [WIA],EnumDeviceInfo method, IWiaDevMgr.EnumDeviceInfo, IWiaDevMgr::EnumDeviceInfo, _wia_IWiaDevMgr_EnumDeviceInfo, wia._wia_IWiaDevMgr_EnumDeviceInfo, wia_xp/IWiaDevMgr::EnumDeviceInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.redist: 
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDevMgr.EnumDeviceInfo
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDevMgr::EnumDeviceInfo


## -description


Applications use the <b>IWiaDevMgr::EnumDeviceInfo</b> method to enumerate property information for each available Windows Image Acquisition (WIA) device.


## -parameters




### -param lFlag [in]

Type: <b>LONG</b>

Specifies the types of WIA devices to enumerate. Should be set to WIA_DEVINFO_ENUM_LOCAL.


### -param ppIEnum [out, retval]

Type: <b><a href="https://msdn.microsoft.com/2133b9a4-9340-4984-a81e-66587f2e5163">IEnumWIA_DEV_INFO</a>**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/2133b9a4-9340-4984-a81e-66587f2e5163">IEnumWIA_DEV_INFO</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IWiaDevMgr::EnumDeviceInfo</b> method creates an enumerator object, that supports the <a href="https://msdn.microsoft.com/2133b9a4-9340-4984-a81e-66587f2e5163">IEnumWIA_DEV_INFO</a> interface. <b>IWiaDevMgr::EnumDeviceInfo</b> stores a pointer to the <b>IEnumWIA_DEV_INFO</b> interface in the parameter <i>ppIEnum</i>. Applications can use the <b>IEnumWIA_DEV_INFO</b> interface pointer to enumerate the properties of each WIA device attached to the user's computer.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnum</i> parameter.



