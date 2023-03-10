---
UID: NF:pla.IDataCollectorSet.get_DisplayName
title: IDataCollectorSet::get_DisplayName (pla.h)
description: Retrieves or sets the display name of the data collector set. (Get)
helpviewer_keywords: ["DisplayName property [PLA]","DisplayName property [PLA]","IDataCollectorSet interface","IDataCollectorSet interface [PLA]","DisplayName property","IDataCollectorSet.DisplayName","IDataCollectorSet.get_DisplayName","IDataCollectorSet::DisplayName","IDataCollectorSet::get_DisplayName","IDataCollectorSet::put_DisplayName","get_DisplayName","pla.idatacollectorset_displayname","pla/IDataCollectorSet::DisplayName","pla/IDataCollectorSet::get_DisplayName","pla/IDataCollectorSet::put_DisplayName"]
old-location: pla\idatacollectorset_displayname.htm
tech.root: PLA
ms.assetid: 4be6d1a1-54de-45fa-8d00-36f8b95e30a5
ms.date: 12/05/2018
ms.keywords: DisplayName property [PLA], DisplayName property [PLA],IDataCollectorSet interface, IDataCollectorSet interface [PLA],DisplayName property, IDataCollectorSet.DisplayName, IDataCollectorSet.get_DisplayName, IDataCollectorSet::DisplayName, IDataCollectorSet::get_DisplayName, IDataCollectorSet::put_DisplayName, get_DisplayName, pla.idatacollectorset_displayname, pla/IDataCollectorSet::DisplayName, pla/IDataCollectorSet::get_DisplayName, pla/IDataCollectorSet::put_DisplayName
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
 - IDataCollectorSet::get_DisplayName
 - pla/IDataCollectorSet::get_DisplayName
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
 - IDataCollectorSet.DisplayName
 - IDataCollectorSet.get_DisplayName
 - IDataCollectorSet.put_DisplayName
---

# IDataCollectorSet::get_DisplayName


## -description

Retrieves or sets the display name of the data collector set.

This property is read/write.

## -parameters

## -remarks

To use a localized string from a binary, specify the display name in the form @<i>binary</i>,#<i>id</i> where <i>binary</i> is the EXE or DLL that contains the localized resource string and <i>id</i> is the string resource identifier.

If you set the display name to the @<i>binary</i>,#<i>id</i> form, when you retrieve  the display name you will receive the localized string. To retrieve the display name string that you set, access the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_displaynameunresolved">IDataCollectorSet::DisplayNameUnresolved</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_displaynameunresolved">IDataCollectorSet::DisplayNameUnresolved</a>
