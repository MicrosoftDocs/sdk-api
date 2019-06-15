---
UID: NF:pla.IDataCollectorSet.put_RootPath
title: IDataCollectorSet::put_RootPath (pla.h)
author: windows-sdk-content
description: Retrieves or sets the base path where the subdirectories are created.
old-location: pla\idatacollectorset_get_rootpath.htm
tech.root: PLA
ms.assetid: 42940cec-c76a-433c-9308-f030dacb05a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],RootPath property, IDataCollectorSet.RootPath, IDataCollectorSet.put_RootPath, IDataCollectorSet::RootPath, IDataCollectorSet::get_RootPath, IDataCollectorSet::put_RootPath, RootPath property [PLA], RootPath property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_rootpath, pla.idatacollectorset_get_rootpath, pla/IDataCollectorSet::RootPath, pla/IDataCollectorSet::get_RootPath, pla/IDataCollectorSet::put_RootPath, put_RootPath
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.RootPath
 - IDataCollectorSet.get_RootPath
 - IDataCollectorSet.put_RootPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollectorSet::put_RootPath


## -description


Retrieves or sets the base path where the subdirectories are created.
<div class="alert"><b>Warning</b>  If you change the <b>RootPath</b> property, you should change it to a directory that only contains performance logs. Setting this to another directory, such as the drive root or system root, may cause files to be inadvertently deleted when the logs are cleaned up by the system.</div><div> </div>This property is read/write.


## -parameters


## -remarks



If this property is changed from the default value, the specified directory must exist before the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-start">IDataCollectorSet::Start</a> method is called.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_latestoutputlocation">IDataCollectorSet::LatestOutputLocation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_outputlocation">IDataCollectorSet::OutputLocation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectory">IDataCollectorSet::Subdirectory</a>
 

 

