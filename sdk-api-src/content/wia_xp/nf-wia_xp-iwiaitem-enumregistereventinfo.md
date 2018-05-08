---
UID: NF:wia_xp.IWiaItem.EnumRegisterEventInfo
title: IWiaItem::EnumRegisterEventInfo
author: windows-driver-content
description: The IWiaItem::EnumRegisterEventInfo method creates an enumerator used to obtain information about events for which an application is registered.
old-location: wia\_wia_IWiaItem_EnumRegisterEventInfo.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\enumregistereventinfo.htm
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: EnumRegisterEventInfo, EnumRegisterEventInfo method [WIA], EnumRegisterEventInfo method [WIA],IWiaItem interface, IWiaItem interface [WIA],EnumRegisterEventInfo method, IWiaItem.EnumRegisterEventInfo, IWiaItem::EnumRegisterEventInfo, _wia_IWiaItem_EnumRegisterEventInfo, wia._wia_IWiaItem_EnumRegisterEventInfo, wia_xp/IWiaItem::EnumRegisterEventInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IWiaItem.EnumRegisterEventInfo
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaItem::EnumRegisterEventInfo


## -description


The <b>IWiaItem::EnumRegisterEventInfo</b> method creates an enumerator used to obtain information about events for which an application is registered.


## -parameters




### -param lFlags [in]

Type: <b>LONG</b>

Currently unused. Should be set to zero.


### -param pEventGUID [in]

Type: <b>const GUID*</b>

Pointer to an identifier that specifies the hardware event for which you want registration information.


### -param ppIEnum [out]

Type: <b><a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a>**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An application invokes this method to create an enumerator object for the event information. <b>IWiaItem::EnumRegisterEventInfo</b> stores the address of the <a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a> interface of the enumerator object in the <i>ppIEnum</i> parameter. The program then uses the interface pointer to enumerate the properties of the event for which it is registered.

Each <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structure includes an indication of whether the event is of type WIA_NOTIFICATION_EVENT or WIA_ACTION_EVENT or both.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnum</i> parameter.



