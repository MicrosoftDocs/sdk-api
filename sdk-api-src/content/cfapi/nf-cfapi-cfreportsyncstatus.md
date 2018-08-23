---
UID: NF:cfapi.CfReportSyncStatus
title: CfReportSyncStatus function
author: windows-sdk-content
description: Allows a sync provider to notify the platform of its status on a specified sync root without having to connect with a call to CfConnectSyncRoot first.
old-location: cloudapi\cfreportsyncstatus.htm
old-project: cfApi
ms.assetid: DC77D18A-CBF4-4172-815A-AB49A48D10B3
ms.author: windowssdkdev
ms.date: 02/27/2018
ms.keywords: CfReportSyncStatus, CfReportSyncStatus function, cfapi/CfReportSyncStatus, cloudApi.cfreportsyncstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CF_UPDATE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfReportSyncStatus
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfReportSyncStatus function


## -description


Allows a sync provider to notify the platform of its status on a specified sync root without having to connect with a call to <a href="https://msdn.microsoft.com/287DA978-9797-48DF-9C90-BA53BB82475C">CfConnectSyncRoot</a> first. 


## -parameters




### -param SyncRootPath [in, out]

Path to the sync root.


### -param SyncStatus [in, out]

The sync status to report; if <b>null</b>, clears the previously-saved sync status. For more information, see the Remarks section, below.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a non-null <a href="https://msdn.microsoft.com/en-us/library/Mt845792(v=VS.85).aspx">CF_SYNC_STATUS</a> is provided in the <i>SyncStatus</i> parameter, the information will be remembered on the sync root until it is cleared explicitly by the sync provider or when the machine reboots. The platform will query this information upon any failed operations on a cloud file placeholder, using the following process:

1.  The platform will first search for sync status at the file level. 

2. If no sync status is found, the platform will then search for sync status registered at the sync root level, which is done through this function.

3.   Once a sync status is located, the platform will use the information provided to construct a more meaningful and actionable message to the user. 


<b>CfReportSyncStatus</b> clears the previously-saved sync status when being called with a <b>null</b> sync status. No change will be made to the existing sync status if the function call fails. 




