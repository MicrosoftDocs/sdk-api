---
UID: NF:pla.IDataCollectorSet.put_Subdirectory
title: IDataCollectorSet::put_Subdirectory (pla.h)
description: Retrieves or sets a base subdirectory of the root path where the next instance of the data collector set will write its logs. (Put)
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Subdirectory property","IDataCollectorSet.Subdirectory","IDataCollectorSet.put_Subdirectory","IDataCollectorSet::Subdirectory","IDataCollectorSet::get_Subdirectory","IDataCollectorSet::put_Subdirectory","Subdirectory property [PLA]","Subdirectory property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_subdirectory","pla.idatacollectorset_get_subdirectory","pla/IDataCollectorSet::Subdirectory","pla/IDataCollectorSet::get_Subdirectory","pla/IDataCollectorSet::put_Subdirectory","put_Subdirectory"]
old-location: pla\idatacollectorset_get_subdirectory.htm
tech.root: PLA
ms.assetid: c2c55fd9-3b29-46be-9792-acb095b1c0e4
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Subdirectory property, IDataCollectorSet.Subdirectory, IDataCollectorSet.put_Subdirectory, IDataCollectorSet::Subdirectory, IDataCollectorSet::get_Subdirectory, IDataCollectorSet::put_Subdirectory, Subdirectory property [PLA], Subdirectory property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_subdirectory, pla.idatacollectorset_get_subdirectory, pla/IDataCollectorSet::Subdirectory, pla/IDataCollectorSet::get_Subdirectory, pla/IDataCollectorSet::put_Subdirectory, put_Subdirectory
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
 - IDataCollectorSet::put_Subdirectory
 - pla/IDataCollectorSet::put_Subdirectory
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
 - IDataCollectorSet.Subdirectory
 - IDataCollectorSet.get_Subdirectory
 - IDataCollectorSet.put_Subdirectory
---

# IDataCollectorSet::put_Subdirectory


## -description

Retrieves or sets a base subdirectory of the root path where the next instance of the data collector set will write its logs.

This property is read/write.

## -parameters

## -remarks

The actual name of the subdirectory used can be different if you had previously specified formatting options in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectoryformat">IDataCollectorSet::SubdirectoryFormat</a> property. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_latestoutputlocation">IDataCollectorSet::LatestOutputLocation</a> property contains the actual folder name used. 

If a location is not specified, files are written to the path specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">IDataCollectorSet::RootPath</a> property.

PLA creates the folders in the subdirectory path if they do not exist. Note that the folders will not inherit the ACLs from the root path. The user specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_useraccount">IDataCollectorSet::UserAccount</a> property and those in the Administrators group will have read and write access to the folders. Users in the Performance Log Users group and Performance Monitor Users group have read-only access.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_latestoutputlocation">IDataCollectorSet::LatestOutputLocation</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_outputlocation">IDataCollectorSet::OutputLocation</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">IDataCollectorSet::RootPath</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectoryformat">IDataCollectorSet::SubdirectoryFormat</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectoryformatpattern">IDataCollectorSet::SubdirectoryFormatPattern</a>
