---
UID: NF:msdrm.DRMIsActivated
title: DRMIsActivated function
author: windows-sdk-content
description: Indicates whether the current user or machine is activated.
old-location: rm\drmisactivated.htm
old-project: AdRms_Sdk
ms.assetid: f6c7bc7f-e9e8-4fc4-b30f-31bc0f5f46aa
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMIsActivated, DRMIsActivated function [Active Directory Rights Management Services SDK 1.0], DRM_ACTIVATE_GROUPIDENTITY, DRM_ACTIVATE_MACHINE, msdrm/DRMIsActivated, rm.drmisactivated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMIsActivated
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMIsActivated function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMIsActivated</b> function indicates whether the current user or machine is activated.


## -parameters




### -param hClient [in]

A handle to a client session created by using the <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a> function.


### -param uFlags [in]

A value that determines whether the current user or machine is being queried for activation status. This can be one of the following values.



#### DRM_ACTIVATE_MACHINE

The machine is being queried for activation status. The machine is considered activated if there is a valid lockbox for the logged-on user 
and a valid <a href="https://www.bing.com/search?q=machine+certificates">machine certificates</a> in the per-user certificate store.

In Rights Management Services client 1.0, the machine is considered activated if there is a valid lockbox 
and a valid <a href="https://www.bing.com/search?q=machine+certificate">machine certificate</a>.



#### DRM_ACTIVATE_GROUPIDENTITY

The current user is being queried for activation status.

The current user is considered activated if the certificate store of the current user has a <a href="https://www.bing.com/search?q=rights+account+certificate">rights account certificate</a> issued to the specified group ID.


### -param pActServInfo [in]

This parameter is reserved and must be set to <b>NULL</b>.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You can call <b>DRMIsActivated</b> to determine the current state of computer or user activation before calling any function that requires prior activation. If <b>DRMIsActivated</b> fails, call <a href="https://msdn.microsoft.com/d3f4ac2c-95d9-4273-a679-81670dd62d28">DRMActivate</a>.

This function internally uses information contained in the client session. If the user ID associated with the client session does not match the ID of the logged–on user, this function will fail. For more information, see <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/f6980a9b-9e3c-47e4-b1c3-7e244ca77e44">Activating a Computer</a>



<a href="https://msdn.microsoft.com/c998647b-2e0c-4eee-bcf9-6c080340f5bb">Activating a User</a>



<a href="https://msdn.microsoft.com/d3f4ac2c-95d9-4273-a679-81670dd62d28">DRMActivate</a>
 

 

