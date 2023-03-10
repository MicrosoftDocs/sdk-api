---
UID: NF:pla.IDataCollectorSet.get_DisplayNameUnresolved
title: IDataCollectorSet::get_DisplayNameUnresolved (pla.h)
description: Retrieves the display name of the data collector set in its original form.
helpviewer_keywords: ["DisplayNameUnresolved property [PLA]","DisplayNameUnresolved property [PLA]","IDataCollectorSet interface","IDataCollectorSet interface [PLA]","DisplayNameUnresolved property","IDataCollectorSet.DisplayNameUnresolved","IDataCollectorSet.get_DisplayNameUnresolved","IDataCollectorSet::DisplayNameUnresolved","IDataCollectorSet::get_DisplayNameUnresolved","get_DisplayNameUnresolved","pla.idatacollectorset_displaynameunresolved","pla/IDataCollectorSet::DisplayNameUnresolved","pla/IDataCollectorSet::get_DisplayNameUnresolved"]
old-location: pla\idatacollectorset_displaynameunresolved.htm
tech.root: PLA
ms.assetid: 47941406-e05d-4a64-9a84-8aa7162e5b48
ms.date: 12/05/2018
ms.keywords: DisplayNameUnresolved property [PLA], DisplayNameUnresolved property [PLA],IDataCollectorSet interface, IDataCollectorSet interface [PLA],DisplayNameUnresolved property, IDataCollectorSet.DisplayNameUnresolved, IDataCollectorSet.get_DisplayNameUnresolved, IDataCollectorSet::DisplayNameUnresolved, IDataCollectorSet::get_DisplayNameUnresolved, get_DisplayNameUnresolved, pla.idatacollectorset_displaynameunresolved, pla/IDataCollectorSet::DisplayNameUnresolved, pla/IDataCollectorSet::get_DisplayNameUnresolved
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollectorSet::get_DisplayNameUnresolved
 - pla/IDataCollectorSet::get_DisplayNameUnresolved
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.DisplayNameUnresolved
 - IDataCollectorSet.get_DisplayNameUnresolved
---

# IDataCollectorSet::get_DisplayNameUnresolved


## -description

Retrieves the display name of the data collector set in its original form.

This property is read-only.

## -parameters

## -remarks

This property returns the display name as you originally set it in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_displayname">IDataCollectorSet::DisplayName</a> property. Typically, you would use this property if you set the display name using the form @<i>binary</i>,#<i>id</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_displayname">IDataCollectorSet::DisplayName</a>