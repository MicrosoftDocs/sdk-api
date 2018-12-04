---
UID: NF:mmc.IConsole.QueryConsoleVerb
title: IConsole::QueryConsoleVerb
author: windows-sdk-content
description: Queries for the IConsoleVerb interface.
old-location: mmc\iconsole_queryconsoleverb.htm
tech.root: mmc
ms.assetid: 6C40014C-EBCC-455C-A575-4637B253439C
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IConsole interface [MMC],QueryConsoleVerb method, IConsole.QueryConsoleVerb, IConsole::QueryConsoleVerb, QueryConsoleVerb, QueryConsoleVerb method [MMC], QueryConsoleVerb method [MMC],IConsole interface, mmc.iconsole_queryconsoleverb, mmc/IConsole::QueryConsoleVerb
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole.QueryConsoleVerb
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsole::QueryConsoleVerb


## -description


Queries for the 
<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a> interface.


## -parameters




### -param ppConsoleVerb [out]

A pointer to the address of a variable that receives the 
<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a> interface pointer.


## -returns



This method can return one of these values.




## -remarks



This method should be called from an 
<a href="https://msdn.microsoft.com/edd98f5e-e251-40ff-8136-02bf1b9ea670">IConsole</a> interface pointer obtained through the 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/edd98f5e-e251-40ff-8136-02bf1b9ea670">IConsole</a>



<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a>
 

 

