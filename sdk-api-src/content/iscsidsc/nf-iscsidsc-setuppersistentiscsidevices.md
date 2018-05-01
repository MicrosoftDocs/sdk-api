---
UID: NF:iscsidsc.SetupPersistentIScsiDevices
title: SetupPersistentIScsiDevices function
author: windows-driver-content
description: SetupPersistentIscsiDevices function builds the list of devices and volumes assigned to iSCSI targets that are connected to the computer, and saves this list in non-volatile cache of the iSCSI initiator service.
old-location: iscsidisc\setuppersistentiscsidevices.htm
old-project: iSCSIDisc
ms.assetid: b21e5872-24b2-4a4c-86a7-528789c1b9aa
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: SetupPersistentIScsiDevices, SetupPersistentIscsiDevices, SetupPersistentIscsiDevices function [iSCSI Discovery Library API], iscsidisc.setuppersistentiscsidevices, iscsidsc/SetupPersistentIscsiDevices
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
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iscsidsc.dll
api_name:
-	SetupPersistentIscsiDevices
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetupPersistentIScsiDevices function


## -description


The <b>SetupPersistentIscsiDevices</b> function builds the list of devices and volumes assigned to iSCSI targets that are connected to the computer, and saves this list in non-volatile cache of the iSCSI initiator service.



## -parameters






## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



When the iSCSI Initiator service starts, it does not complete initialization until the storage stack can access and enumerate all persistent iSCSI volumes and devices. If there is a service that is dependent on data stored on a persistent volume or device, it should be configured to have a dependency on the iSCSI service (MSiSCSI).

The correct procedure for a system administrator to configure a computer to use external persistent volumes is as follows:

 

 


 



<ul>
<li>Login to all of the targets that contain the volumes</li>
<li>Configure all volumes on top of the disks</li>
<li>Use management software to call the <b>SetupPersistentIscsiDevices</b> routine, so that the iSCSI initiator service will add the volumes to its list of persistent volumes.</li>
</ul>


