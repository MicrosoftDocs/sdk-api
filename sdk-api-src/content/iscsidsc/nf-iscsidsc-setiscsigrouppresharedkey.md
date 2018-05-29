---
UID: NF:iscsidsc.SetIScsiGroupPresharedKey
title: SetIScsiGroupPresharedKey function
author: windows-sdk-content
description: SetIscsiGroupPresharedKey function establishes the default group preshared key for all initiators on the computer.
old-location: iscsidisc\setiscsigrouppresharedkey.htm
old-project: iSCSIDisc
ms.assetid: 344d0a88-64e9-45a3-a789-6733b85e9c2d
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: SetIScsiGroupPresharedKey, SetIscsiGroupPresharedKey, SetIscsiGroupPresharedKey function [iSCSI Discovery Library API], iscsidisc.setiscsigrouppresharedkey, iscsidsc/SetIscsiGroupPresharedKey
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
-	SetIscsiGroupPresharedKey
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetIScsiGroupPresharedKey function


## -description


The <b>SetIscsiGroupPresharedKey</b> function establishes the default group preshared key for all initiators on the computer.



## -parameters




### -param KeyLength [in]

The size, in bytes, of the preshared key. 


### -param Key [in]

The buffer that contains the preshared key.


### -param Persist

If <b>true</b>, this parameter indicates that the preshared key information will be stored in non-volatile memory and will persist across restarts of the computer or the iSCSI initiator service. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.




