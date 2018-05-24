---
UID: NF:shobjidl.ITrayDeskBand.DeskBandRegistrationChanged
title: ITrayDeskBand::DeskBandRegistrationChanged
author: windows-driver-content
description: Refreshes the deskband registration cache.
old-location: shell\ITrayDeskBand_DeskBandRegistrationChanged.htm
old-project: shell
ms.assetid: 912ae157-984e-4255-ac1e-e1e7b0b92c15
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DeskBandRegistrationChanged, DeskBandRegistrationChanged method [Windows Shell], DeskBandRegistrationChanged method [Windows Shell],ITrayDeskBand interface, ITrayDeskBand interface [Windows Shell],DeskBandRegistrationChanged method, ITrayDeskBand.DeskBandRegistrationChanged, ITrayDeskBand::DeskBandRegistrationChanged, _shell_ITrayDeskBand_DeskBandRegistrationChanged, shell.ITrayDeskBand_DeskBandRegistrationChanged, shobjidl/ITrayDeskBand::DeskBandRegistrationChanged
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
-	ITrayDeskBand.DeskBandRegistrationChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ITrayDeskBand::DeskBandRegistrationChanged


## -description


Refreshes the deskband registration cache.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method immediately after making a change to the deskband registration. For example, through the CLSID_StdComponentCategoriesMgr object.



