---
UID: NF:setupapi.SetupDiGetHwProfileFriendlyNameA
title: SetupDiGetHwProfileFriendlyNameA function
author: windows-sdk-content
description: The SetupDiGetHwProfileFriendlyName function retrieves the friendly name associated with a hardware profile ID.
old-location: devinst\setupdigethwprofilefriendlyname.htm
tech.root: devinst
ms.assetid: 92f08c8a-b31a-4f88-8ff5-c60d985b79bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupDiGetHwProfileFriendlyName, SetupDiGetHwProfileFriendlyName function [Device and Driver Installation], SetupDiGetHwProfileFriendlyNameA, SetupDiGetHwProfileFriendlyNameW, devinst.setupdigethwprofilefriendlyname, di-rtns_3a055603-6e43-449a-bfd0-fbd7434bebfe.xml, setupapi/SetupDiGetHwProfileFriendlyName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetHwProfileFriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiGetHwProfileFriendlyNameA function


## -description


The <b>SetupDiGetHwProfileFriendlyName</b> function retrieves the friendly name associated with a hardware profile ID.


## -parameters




### -param HwProfile [in]

The hardware profile ID associated with the friendly name to retrieve. If this parameter is 0, the friendly name for the current hardware profile is retrieved.


### -param FriendlyName [out]

A pointer to a string buffer to receive the friendly name.


### -param FriendlyNameSize [in]

The size, in characters, of the <i>FriendlyName</i> buffer.


### -param RequiredSize [out, optional]

A pointer to a variable of type DWORD that receives the number of characters required to retrieve the friendly name (including a NULL terminator).


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Call <a href="https://msdn.microsoft.com/839c1e4c-cfa6-4f59-979c-24623a040d5c">SetupDiGetHwProfileFriendlyNameEx</a> to get the friendly name of a hardware profile ID on a remote computer.




## -see-also




<a href="https://msdn.microsoft.com/839c1e4c-cfa6-4f59-979c-24623a040d5c">SetupDiGetHwProfileFriendlyNameEx</a>



<a href="https://msdn.microsoft.com/59fc7202-0e03-4eaa-b3ca-7d55be767b1a">SetupDiGetHwProfileList</a>
 

 

