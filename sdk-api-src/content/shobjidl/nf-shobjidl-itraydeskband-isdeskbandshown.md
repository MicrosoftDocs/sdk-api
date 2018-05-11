---
UID: NF:shobjidl.ITrayDeskBand.IsDeskBandShown
title: ITrayDeskBand::IsDeskBandShown
author: windows-driver-content
description: Indicates whether a deskband is shown.
old-location: shell\ITrayDeskBand_IsDeskBandShown.htm
old-project: shell
ms.assetid: 969b8a91-6685-4fd8-95a1-bb9f0bfc88b5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ITrayDeskBand interface [Windows Shell],IsDeskBandShown method, ITrayDeskBand.IsDeskBandShown, ITrayDeskBand::IsDeskBandShown, IsDeskBandShown, IsDeskBandShown method [Windows Shell], IsDeskBandShown method [Windows Shell],ITrayDeskBand interface, _shell_ITrayDeskBand_IsDeskBandShown, shell.ITrayDeskBand_IsDeskBandShown, shobjidl/ITrayDeskBand::IsDeskBandShown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	ITrayDeskBand.IsDeskBandShown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ITrayDeskBand::IsDeskBandShown


## -description


Indicates whether a deskband is shown.


## -parameters




### -param clsid [in]

Type: <b>REFCLSID</b>

A reference to a deskband CLSID.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the deskband is shown, S_FALSE if the deskband is not shown, or an error value otherwise.



