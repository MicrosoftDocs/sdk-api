---
UID: NF:pla.IDataCollectorSet.get_LatestOutputLocation
title: IDataCollectorSet::get_LatestOutputLocation (pla.h)
description: Retrieves or sets the fully decorated folder name that PLA used the last time logs were written. (IDataCollectorSet.get_LatestOutputLocation)
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","LatestOutputLocation property","IDataCollectorSet.LatestOutputLocation","IDataCollectorSet.get_LatestOutputLocation","IDataCollectorSet::LatestOutputLocation","IDataCollectorSet::get_LatestOutputLocation","IDataCollectorSet::put_LatestOutputLocation","LatestOutputLocation property [PLA]","LatestOutputLocation property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_latestoutputlocation","get_LatestOutputLocation","pla.idatacollectorset_get_latestoutputlocation","pla/IDataCollectorSet::LatestOutputLocation","pla/IDataCollectorSet::get_LatestOutputLocation","pla/IDataCollectorSet::put_LatestOutputLocation"]
old-location: pla\idatacollectorset_get_latestoutputlocation.htm
tech.root: PLA
ms.assetid: c0047144-5f99-4acd-ad96-054afcbe6eb9
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],LatestOutputLocation property, IDataCollectorSet.LatestOutputLocation, IDataCollectorSet.get_LatestOutputLocation, IDataCollectorSet::LatestOutputLocation, IDataCollectorSet::get_LatestOutputLocation, IDataCollectorSet::put_LatestOutputLocation, LatestOutputLocation property [PLA], LatestOutputLocation property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_latestoutputlocation, get_LatestOutputLocation, pla.idatacollectorset_get_latestoutputlocation, pla/IDataCollectorSet::LatestOutputLocation, pla/IDataCollectorSet::get_LatestOutputLocation, pla/IDataCollectorSet::put_LatestOutputLocation
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
 - IDataCollectorSet::get_LatestOutputLocation
 - pla/IDataCollectorSet::get_LatestOutputLocation
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
 - IDataCollectorSet.LatestOutputLocation
 - IDataCollectorSet.get_LatestOutputLocation
 - IDataCollectorSet.put_LatestOutputLocation
---

# IDataCollectorSet::get_LatestOutputLocation


## -description

Retrieves or sets the fully decorated folder name that PLA used the last time logs were written.

This property is read/write.

## -parameters

## -remarks

Typically, you do not set this property. When the data collector starts, PLA sets this property using the value from the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_outputlocation">IDataCollectorSet::OutputLocation</a> property.

You can set this property to empty if the folder has been deleted.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_outputlocation">IDataCollectorSet::OutputLocation</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">IDataCollectorSet::RootPath</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectory">IDataCollectorSet::Subdirectory</a>
