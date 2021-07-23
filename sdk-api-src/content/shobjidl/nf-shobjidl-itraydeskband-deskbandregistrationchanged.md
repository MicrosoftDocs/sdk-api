---
UID: NF:shobjidl.ITrayDeskBand.DeskBandRegistrationChanged
title: ITrayDeskBand::DeskBandRegistrationChanged (shobjidl.h)
description: Refreshes the deskband registration cache.
helpviewer_keywords: ["DeskBandRegistrationChanged","DeskBandRegistrationChanged method [Windows Shell]","DeskBandRegistrationChanged method [Windows Shell]","ITrayDeskBand interface","ITrayDeskBand interface [Windows Shell]","DeskBandRegistrationChanged method","ITrayDeskBand.DeskBandRegistrationChanged","ITrayDeskBand::DeskBandRegistrationChanged","_shell_ITrayDeskBand_DeskBandRegistrationChanged","shell.ITrayDeskBand_DeskBandRegistrationChanged","shobjidl/ITrayDeskBand::DeskBandRegistrationChanged"]
old-location: shell\ITrayDeskBand_DeskBandRegistrationChanged.htm
tech.root: shell
ms.assetid: 912ae157-984e-4255-ac1e-e1e7b0b92c15
ms.date: 12/05/2018
ms.keywords: DeskBandRegistrationChanged, DeskBandRegistrationChanged method [Windows Shell], DeskBandRegistrationChanged method [Windows Shell],ITrayDeskBand interface, ITrayDeskBand interface [Windows Shell],DeskBandRegistrationChanged method, ITrayDeskBand.DeskBandRegistrationChanged, ITrayDeskBand::DeskBandRegistrationChanged, _shell_ITrayDeskBand_DeskBandRegistrationChanged, shell.ITrayDeskBand_DeskBandRegistrationChanged, shobjidl/ITrayDeskBand::DeskBandRegistrationChanged
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITrayDeskBand::DeskBandRegistrationChanged
 - shobjidl/ITrayDeskBand::DeskBandRegistrationChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - ITrayDeskBand.DeskBandRegistrationChanged
---

# ITrayDeskBand::DeskBandRegistrationChanged


## -description

Refreshes the deskband registration cache.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method immediately after making a change to the deskband registration. For example, through the CLSID_StdComponentCategoriesMgr object.

