---
UID: NF:wia_xp.IWiaItem.EnumDeviceCapabilities
title: IWiaItem::EnumDeviceCapabilities
author: windows-sdk-content
description: The IWiaItem::EnumDeviceCapabilities method creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) device supports.
old-location: wia\_wia_IWiaItem_EnumDeviceCapabilities.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\enumdevicecapabilities.htm
ms.author: windowssdkdev
ms.date: 05/03/2018
ms.keywords: EnumDeviceCapabilities, EnumDeviceCapabilities method [WIA], EnumDeviceCapabilities method [WIA],IWiaItem interface, IWiaItem interface [WIA],EnumDeviceCapabilities method, IWiaItem.EnumDeviceCapabilities, IWiaItem::EnumDeviceCapabilities, _wia_IWiaItem_EnumDeviceCapabilities, wia._wia_IWiaItem_EnumDeviceCapabilities, wia_xp/IWiaItem::EnumDeviceCapabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaservc.dll
api_name:
-	IWiaItem.EnumDeviceCapabilities
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaItem::EnumDeviceCapabilities


## -description


The <b>IWiaItem::EnumDeviceCapabilities</b> method creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) device supports.


## -parameters




### -param lFlags [in]

Type: <b>LONG</b>

Specifies a flag that selects the type of capabilities to enumerate. Can be set to one or more of the following values:



<table class="clsStd">
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>WIA_DEVICE_COMMANDS</td>
<td>Enumerate device commands.</td>
</tr>
<tr>
<td>WIA_DEVICE_EVENTS</td>
<td>Enumerate device events.</td>
</tr>
</table>
 


### -param ppIEnumWIA_DEV_CAPS [out]

Type: <b><a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a>**</b>

Pointer to <a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a> interface created by <b>IWiaItem::EnumDeviceCapabilities</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use this method to create an enumerator object to obtain the set of commands and events that a WIA device supports. You can use the <i>lFlags</i> parameter to specify which kinds of device capabilities to enumerate. The <b>IWiaItem::EnumDeviceCapabilities</b> method stores the address of the interface of the enumerator object in the <i>ppIEnumWIA_DEV_CAPS</i> parameter.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnumWIA_DEV_CAPS</i> parameter.



