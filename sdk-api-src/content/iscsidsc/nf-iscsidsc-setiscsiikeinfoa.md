---
UID: NF:iscsidsc.SetIScsiIKEInfoA
title: SetIScsiIKEInfoA function
author: windows-driver-content
description: SetIscsiIKEInfo function establishes the IPsec policy and preshared key for the indicated initiator to use when performing iSCSI connections.
old-location: iscsidisc\setiscsiikeinfo.htm
old-project: iSCSIDisc
ms.assetid: db020346-45cf-4944-9776-81bb38c7ee6a
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: SetIScsiIKEInfoA, SetIscsiIKEInfo, SetIscsiIKEInfo function [iSCSI Discovery Library API], SetIscsiIKEInfoA, SetIscsiIKEInfoW, iscsidisc.setiscsiikeinfo, iscsidsc/SetIscsiIKEInfo, iscsidsc/SetIscsiIKEInfoA, iscsidsc/SetIscsiIKEInfoW
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
req.unicode-ansi: SetIscsiIKEInfoW (Unicode) and SetIscsiIKEInfoA (ANSI)
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
-	SetIscsiIKEInfo
-	SetIscsiIKEInfoA
-	SetIscsiIKEInfoW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetIScsiIKEInfoA function


## -description


The <b>SetIscsiIKEInfo</b> function establishes the IPsec policy and preshared key for the indicated initiator to use when performing iSCSI connections.



## -parameters




### -param InitiatorName [in]

The name of the initiator HBA for which the IPsec policy is established.


### -param InitiatorPortNumber

TBD


### -param AuthInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/d61036f5-a5e8-4c1a-8f99-57fe8e5c5bd0">IKE_AUTHENTICATION_INFORMATION</a> structure that contains the authentication method. Currently, only the IKE_AUTHENTICATION_PRESHARED_KEY_METHOD is supported. 



### -param Persist [in]

If <b>true</b>, this parameter indicates that the preshared key information will be stored in non-volatile memory and will persist across restarts of the computer or the iSCSI initiator service. 


#### - PortNumber [in]

The port on the initiator HBA with which to associate the key. If this parameter contains a value of <b>ISCSI_ALL_INITIATOR_PORTS</b>, all ports on the initiator are associated with the key.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -see-also




<a href="https://msdn.microsoft.com/81576452-47bf-4732-a09f-dd1f9e2689c9">GetIscsiIKEInfo</a>



<a href="https://msdn.microsoft.com/d61036f5-a5e8-4c1a-8f99-57fe8e5c5bd0">IKE_AUTHENTICATION_INFORMATION</a>
 

 

