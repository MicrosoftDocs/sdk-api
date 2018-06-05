---
UID: NF:pla.IDataCollectorSet.SetCredentials
title: IDataCollectorSet::SetCredentials
author: windows-sdk-content
description: Specifies the user account under which the data collector set runs.
old-location: pla\idatacollectorset_setcredentials.htm
old-project: PLA
ms.assetid: 39275154-fe85-492e-9d64-79d17cb4f88d
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDataCollectorSet interface [PLA],SetCredentials method, IDataCollectorSet.SetCredentials, IDataCollectorSet::SetCredentials, SetCredentials, SetCredentials method [PLA], SetCredentials method [PLA],IDataCollectorSet interface, base.idatacollectorset_setcredentials, pla.idatacollectorset_setcredentials, pla/IDataCollectorSet::SetCredentials
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: pla.h
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
tech.root: 
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IDataCollectorSet.SetCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IDataCollectorSet::SetCredentials


## -description


Specifies the user account under which the data collector set runs.  


## -parameters




### -param user [in]

A user account under which the data collector set runs. Specify the user name in the form <i>domain</i>\<i>user</i> or <i>user</i>@<i>domain</i>.


### -param password [in]

The password of the user account.


## -returns



The property returns S_OK if successful.




## -remarks



To clear the user credentials, set both parameters to <b>NULL</b>.

If you do not specify the credentials, PLA tries to run the set as LocalSystem if the current user is a member of the administrator group. 




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/32fe1dcf-9682-40fd-b301-45385fa33cbe">IDataCollectorSet::UserAccount</a>
 

 

