---
UID: NF:pla.IDataCollectorSet.put_Description
title: IDataCollectorSet::put_Description (pla.h)
description: Retrieves or sets the description of the data collector set. The description will be added to all output files as metadata and inserted into Performance Data Helper logs as a comment. (Put)
helpviewer_keywords: ["Description property [PLA]","Description property [PLA]","IDataCollectorSet interface","IDataCollectorSet interface [PLA]","Description property","IDataCollectorSet.Description","IDataCollectorSet.put_Description","IDataCollectorSet::Description","IDataCollectorSet::get_Description","IDataCollectorSet::put_Description","base.idatacollectorset_get_description","pla.idatacollectorset_get_description","pla/IDataCollectorSet::Description","pla/IDataCollectorSet::get_Description","pla/IDataCollectorSet::put_Description","put_Description"]
old-location: pla\idatacollectorset_get_description.htm
tech.root: PLA
ms.assetid: d36deb28-09fa-4efd-bfe8-055757f4273a
ms.date: 12/05/2018
ms.keywords: Description property [PLA], Description property [PLA],IDataCollectorSet interface, IDataCollectorSet interface [PLA],Description property, IDataCollectorSet.Description, IDataCollectorSet.put_Description, IDataCollectorSet::Description, IDataCollectorSet::get_Description, IDataCollectorSet::put_Description, base.idatacollectorset_get_description, pla.idatacollectorset_get_description, pla/IDataCollectorSet::Description, pla/IDataCollectorSet::get_Description, pla/IDataCollectorSet::put_Description, put_Description
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
 - IDataCollectorSet::put_Description
 - pla/IDataCollectorSet::put_Description
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
 - IDataCollectorSet.Description
 - IDataCollectorSet.get_Description
 - IDataCollectorSet.put_Description
---

# IDataCollectorSet::put_Description


## -description

Retrieves or sets the description of the data collector set.  The description will be added to all output files as metadata and inserted into Performance Data Helper logs as a comment.

This property is read/write.

## -parameters

## -remarks

To use a localized string from a binary, specify the description in the form @<i>binary</i>,#<i>id</i> where <i>binary</i> is the EXE or DLL that contains the localized resource string and <i>id</i> is the string resource identifier.

If you set the description to the @<i>binary</i>,#<i>id</i> form, when you retrieve  the description you will receive the localized string. To retrieve the description string that you set, access the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_descriptionunresolved">IDataCollectorSet::DescriptionUnresolved</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_descriptionunresolved">IDataCollectorSet::DescriptionUnresolved</a>
