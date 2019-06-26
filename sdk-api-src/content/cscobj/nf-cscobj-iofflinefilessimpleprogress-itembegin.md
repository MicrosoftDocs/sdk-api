---
UID: NF:cscobj.IOfflineFilesSimpleProgress.ItemBegin
title: IOfflineFilesSimpleProgress::ItemBegin (cscobj.h)
author: windows-sdk-content
description: Reports that an operation on an item is beginning.
old-location: of\iofflinefilessimpleprogress_itembegin.htm
tech.root: offlinefiles
ms.assetid: 0e3496ee-e987-4c37-93ff-bc8409acabde
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSimpleProgress interface [Offline Files],ItemBegin method, IOfflineFilesSimpleProgress.ItemBegin, IOfflineFilesSimpleProgress::ItemBegin, ItemBegin, ItemBegin method [Offline Files], ItemBegin method [Offline Files],IOfflineFilesSimpleProgress interface, cscobj/IOfflineFilesSimpleProgress::ItemBegin, of.iofflinefilessimpleprogress_itembegin
ms.topic: method
f1_keywords: 
 - "cscobj/IOfflineFilesSimpleProgress.ItemBegin"
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSimpleProgress.ItemBegin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSimpleProgress::ItemBegin


## -description


Reports that an operation on an item is beginning.


## -parameters




### -param pszFile [in]

Receives the fully qualified UNC path of the file or directory that is being processed.


### -param pResponse [out]

Set this parameter to a value from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/ne-cscobj-tagofflinefiles_op_response">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed


## -returns



The return value is ignored.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessimpleprogress">IOfflineFilesSimpleProgress</a>
 

 

