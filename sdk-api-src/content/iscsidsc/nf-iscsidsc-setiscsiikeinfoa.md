---
UID: NF:iscsidsc.SetIScsiIKEInfoA
title: SetIScsiIKEInfoA function (iscsidsc.h)
author: windows-sdk-content
description: SetIscsiIKEInfo function establishes the IPsec policy and preshared key for the indicated initiator to use when performing iSCSI connections.
old-location: iscsidisc\setiscsiikeinfo.htm
tech.root: iSCSIDisc
ms.assetid: db020346-45cf-4944-9776-81bb38c7ee6a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetIScsiIKEInfoA, SetIscsiIKEInfo, SetIscsiIKEInfo function [iSCSI Discovery Library API], SetIscsiIKEInfoA, SetIscsiIKEInfoW, iscsidisc.setiscsiikeinfo, iscsidsc/SetIscsiIKEInfo, iscsidsc/SetIscsiIKEInfoA, iscsidsc/SetIscsiIKEInfoW
ms.topic: function
f1_keywords: 
 - "iscsidsc/SetIscsiIKEInfo"
dev_langs:
 - c++
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
 - SetIscsiIKEInfo
 - SetIscsiIKEInfoA
 - SetIscsiIKEInfoW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetIScsiIKEInfoA function


## -description


The <b>SetIscsiIKEInfo</b> function establishes the IPsec policy and preshared key for the indicated initiator to use when performing iSCSI connections.



## -parameters




### -param InitiatorName [in]

The name of the initiator HBA for which the IPsec policy is established.


### -param InitiatorPortNumber [in]

The port on the initiator HBA with which to associate the key. If this parameter contains a value of <b>ISCSI_ALL_INITIATOR_PORTS</b>, all ports on the initiator are associated with the key.


### -param AuthInfo [in]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_information">IKE_AUTHENTICATION_INFORMATION</a> structure that contains the authentication method. Currently, only the IKE_AUTHENTICATION_PRESHARED_KEY_METHOD is supported. 



### -param Persist [in]

If <b>true</b>, this parameter indicates that the preshared key information will be stored in non-volatile memory and will persist across restarts of the computer or the iSCSI initiator service. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-getiscsiikeinfoa">GetIscsiIKEInfo</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_information">IKE_AUTHENTICATION_INFORMATION</a>
 

 

