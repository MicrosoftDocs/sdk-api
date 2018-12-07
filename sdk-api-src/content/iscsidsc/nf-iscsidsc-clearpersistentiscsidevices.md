---
UID: NF:iscsidsc.ClearPersistentIScsiDevices
title: ClearPersistentIScsiDevices function
author: windows-sdk-content
description: ClearPersistentIscsiDevices function removes all volumes and devices from the list of persistently bound iSCSI volumes.
old-location: iscsidisc\clearpersistentiscsidevices.htm
tech.root: iSCSIDisc
ms.assetid: 9e21dde6-face-40ae-803b-2aa7861e6f4f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClearPersistentIScsiDevices, ClearPersistentiScsiDevices, ClearPersistentiScsiDevices function [iSCSI Discovery Library API], iscsidisc.clearpersistentiscsidevices, iscsidsc/ClearPersistentiScsiDevices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iscsidsc.h
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
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - ClearPersistentiScsiDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClearPersistentIScsiDevices function


## -description


The <b>ClearPersistentIscsiDevices</b> function removes all volumes and devices from the list of persistently bound iSCSI volumes.




## -parameters






## -returns



returns ERROR_SUCCESS if the operation succeeds and the appropriate Win32 or iSCSI error code if the operation fails.





## -see-also




<a href="https://msdn.microsoft.com/184b256b-0cb0-45c1-8f73-5ff28fb388fb">AddPersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/2522f906-2a91-4d5b-8d6b-86e22c707046">RemoveIscsiPersistentTarget</a>



<a href="https://msdn.microsoft.com/4016d8e4-de67-4c49-b54f-31c1b7bd64a8">RemovePersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/0ab1a864-b44e-4307-9f7c-93cc0d40ff3a">ReportIscsiPersistentLogins</a>



<a href="https://msdn.microsoft.com/856e240d-8c4d-4e55-aef3-71f98193c221">ReportPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/b21e5872-24b2-4a4c-86a7-528789c1b9aa">SetupPersistentIscsiDevices</a>
 

 

