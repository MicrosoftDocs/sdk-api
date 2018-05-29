---
UID: NF:iscsidsc.RemoveIScsiPersistentTargetW
title: RemoveIScsiPersistentTargetW function
author: windows-sdk-content
description: RemoveIscsiPersistentTarget function removes a persistent login for the specified hardware initiator Host Bus Adapter (HBA), initiator port, and target portal.
old-location: iscsidisc\removeiscsipersistenttarget.htm
old-project: iSCSIDisc
ms.assetid: 2522f906-2a91-4d5b-8d6b-86e22c707046
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: RemoveIScsiPersistentTargetW, RemoveIscsiPersistentTarget, RemoveIscsiPersistentTarget function [iSCSI Discovery Library API], RemoveIscsiPersistentTargetA, RemoveIscsiPersistentTargetW, iscsidisc.removeiscsipersistenttarget, iscsidsc/RemoveIscsiPersistentTarget, iscsidsc/RemoveIscsiPersistentTargetA, iscsidsc/RemoveIscsiPersistentTargetW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveIscsiPersistentTargetW (Unicode) and RemoveIscsiPersistentTargetA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iscsidsc.dll
api_name:
-	RemoveIscsiPersistentTarget
-	RemoveIscsiPersistentTargetA
-	RemoveIscsiPersistentTargetW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# RemoveIScsiPersistentTargetW function


## -description


The <b>RemoveIscsiPersistentTarget</b> function removes a persistent login for the specified hardware initiator Host Bus Adapter (HBA), initiator port, and target portal.


## -parameters




### -param InitiatorInstance [in]

The name of the initiator that maintains the persistent login to remove. 


### -param InitiatorPortNumber [in, optional]

The port number on which the initiator connects to <i>TargetName</i>. If <i>InitiatorPortNumber</i> is <b>ISCSI_ALL_INITIATOR_PORTS</b> the miniport driver for the initiator HBA removes the <i>TargetName</i> from the persistent login lists for all initiator ports. 



### -param TargetName [in]

The name of the target.


### -param Portal [in]

The portal through which the initiator connects to the target. If <i>Portal</i> is <b>null</b> or contains no information, the miniport driver for the initiator HBA removes persistent logins for the target on all portals. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -see-also




<a href="https://msdn.microsoft.com/184b256b-0cb0-45c1-8f73-5ff28fb388fb">AddPersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/9e21dde6-face-40ae-803b-2aa7861e6f4f">ClearPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/4016d8e4-de67-4c49-b54f-31c1b7bd64a8">RemovePersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/0ab1a864-b44e-4307-9f7c-93cc0d40ff3a">ReportIscsiPersistentLogins</a>



<a href="https://msdn.microsoft.com/856e240d-8c4d-4e55-aef3-71f98193c221">ReportPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/b21e5872-24b2-4a4c-86a7-528789c1b9aa">SetupPersistentIscsiDevices</a>
 

 

