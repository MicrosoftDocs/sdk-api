---
UID: NF:pla.IDataCollectorSet.get_DescriptionUnresolved
title: IDataCollectorSet::get_DescriptionUnresolved (pla.h)
description: Retrieves the description of the data collector set in its original form.
helpviewer_keywords: ["DescriptionUnresolved property [PLA]","DescriptionUnresolved property [PLA]","IDataCollectorSet interface","IDataCollectorSet interface [PLA]","DescriptionUnresolved property","IDataCollectorSet.DescriptionUnresolved","IDataCollectorSet.get_DescriptionUnresolved","IDataCollectorSet::DescriptionUnresolved","IDataCollectorSet::get_DescriptionUnresolved","get_DescriptionUnresolved","pla.idatacollectorset_descriptionunresolved","pla/IDataCollectorSet::DescriptionUnresolved","pla/IDataCollectorSet::get_DescriptionUnresolved"]
old-location: pla\idatacollectorset_descriptionunresolved.htm
tech.root: PLA
ms.assetid: 153159b2-54dc-477a-92eb-18328ea3351b
ms.date: 12/05/2018
ms.keywords: DescriptionUnresolved property [PLA], DescriptionUnresolved property [PLA],IDataCollectorSet interface, IDataCollectorSet interface [PLA],DescriptionUnresolved property, IDataCollectorSet.DescriptionUnresolved, IDataCollectorSet.get_DescriptionUnresolved, IDataCollectorSet::DescriptionUnresolved, IDataCollectorSet::get_DescriptionUnresolved, get_DescriptionUnresolved, pla.idatacollectorset_descriptionunresolved, pla/IDataCollectorSet::DescriptionUnresolved, pla/IDataCollectorSet::get_DescriptionUnresolved
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
 - IDataCollectorSet::get_DescriptionUnresolved
 - pla/IDataCollectorSet::get_DescriptionUnresolved
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
 - IDataCollectorSet.DescriptionUnresolved
 - IDataCollectorSet.get_DescriptionUnresolved
---

# IDataCollectorSet::get_DescriptionUnresolved


## -description

Retrieves the description of the data collector set in its original form.  

This property is read-only.

## -parameters

## -remarks

This property returns the description as you originally set it in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_description">IDataCollectorSet::Description</a> property. Typically, you would use this property if you set the description using the form @<i>binary</i>,#<i>id</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_description">IDataCollectorSet::Description</a>