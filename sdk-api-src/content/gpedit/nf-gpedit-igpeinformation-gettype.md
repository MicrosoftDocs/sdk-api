---
UID: NF:gpedit.IGPEInformation.GetType
title: IGPEInformation::GetType method
author: windows-driver-content
description: The GetType method retrieves type information for the GPO being edited.
old-location: policy\igpeinformation_gettype.htm
old-project: Policy
ms.assetid: 47769405-d32c-4f4f-86fc-970d89bba848
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GPOTypeDS, GPOTypeLocal, GPOTypeRemote, GetType method [Group Policy], GetType method [Group Policy], IGPEInformation interface, GetType,IGPEInformation.GetType, IGPEInformation, IGPEInformation interface [Group Policy], GetType method, IGPEInformation::GetType, _win32_igpeinformation_gettype, gpedit/IGPEInformation::GetType, policy.igpeinformation_gettype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpedit.dll
api_name:
-	IGPEInformation.GetType
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPEInformation::GetType method


## -description


The
    <b>GetType</b> method retrieves type information for the GPO being edited.


## -parameters




### -param gpoType [out]

Receives the GPO type. The system sets this parameter to one of the following values.



#### GPOTypeLocal

Local



#### GPOTypeRemote

Remote



#### GPOTypeDS

Active Directory


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a>
 

 

