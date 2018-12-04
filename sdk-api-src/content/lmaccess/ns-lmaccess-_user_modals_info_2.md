---
UID: NS:lmaccess._USER_MODALS_INFO_2
title: "_USER_MODALS_INFO_2"
author: windows-sdk-content
description: The USER_MODALS_INFO_2 structure contains the Security Account Manager (SAM) domain name and identifier.
old-location: netmgmt\user_modals_info_2_str.htm
tech.root: netmgmt
ms.assetid: 9a4b3fc1-03b5-4ba7-948f-e455c34fa234
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*LPUSER_MODALS_INFO_2, *PUSER_MODALS_INFO_2, LPUSER_MODALS_INFO_2, LPUSER_MODALS_INFO_2 structure pointer [Network Management], PUSER_MODALS_INFO_2, PUSER_MODALS_INFO_2 structure pointer [Network Management], USER_MODALS_INFO_2, USER_MODALS_INFO_2 structure [Network Management], _USER_MODALS_INFO_2, _win32_user_modals_info_2_str, lmaccess/LPUSER_MODALS_INFO_2, lmaccess/PUSER_MODALS_INFO_2, lmaccess/USER_MODALS_INFO_2, netmgmt.user_modals_info_2_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_MODALS_INFO_2
product: Windows
targetos: Windows
req.typenames: USER_MODALS_INFO_2, *PUSER_MODALS_INFO_2, *LPUSER_MODALS_INFO_2
req.redist: 
---

# _USER_MODALS_INFO_2 structure


## -description


The
				<b>USER_MODALS_INFO_2</b> structure contains the Security Account Manager (SAM) domain name and identifier.


## -struct-fields




### -field usrmod2_domain_name

Specifies the name of the Security Account Manager (SAM) domain. For a domain controller, this is the name of the domain that the controller is a member of. For workstations, this is the name of the computer.


### -field usrmod2_domain_id

Pointer to a 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that contains the security identifier (SID) of the domain named by the <b>usrmod2_domain_name</b> member.


## -see-also




<a href="https://msdn.microsoft.com/5bb18144-82a6-4e9b-8321-c06a667bdd03">NetUserModalsGet</a>



<a href="https://msdn.microsoft.com/9884e076-ee6a-4aca-abe6-a79754667759">NetUserModalsSet</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/e655b9f6-2808-4bd4-998c-c8a2e980920b">User Modal Functions</a>
 

 

