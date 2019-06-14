---
UID: NF:setupapi.SetupDiGetHwProfileFriendlyNameExA
title: SetupDiGetHwProfileFriendlyNameExA function (setupapi.h)
author: windows-sdk-content
description: The SetupDiGetHwProfileFriendlyNameEx function retrieves the friendly name associated with a hardware profile ID on a local or remote computer.
old-location: devinst\setupdigethwprofilefriendlynameex.htm
tech.root: devinst
ms.assetid: 839c1e4c-cfa6-4f59-979c-24623a040d5c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupDiGetHwProfileFriendlyNameEx, SetupDiGetHwProfileFriendlyNameEx function [Device and Driver Installation], SetupDiGetHwProfileFriendlyNameExA, SetupDiGetHwProfileFriendlyNameExW, devinst.setupdigethwprofilefriendlynameex, di-rtns_43d54c1e-047c-491c-93a1-cd5eff918a58.xml, setupapi/SetupDiGetHwProfileFriendlyNameEx
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
 - SetupDiGetHwProfileFriendlyNameEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiGetHwProfileFriendlyNameExA function


## -description


The <b>SetupDiGetHwProfileFriendlyNameEx</b> function retrieves the friendly name associated with a hardware profile ID on a local or remote computer.


## -parameters




### -param HwProfile [in]

Supplies the hardware profile ID associated with the friendly name to retrieve. If this parameter is 0, the friendly name for the current hardware profile is retrieved.


### -param FriendlyName [out]

A pointer to a character buffer to receive the friendly name.


### -param FriendlyNameSize [in]

The size, in characters, of the <i>FriendlyName</i> buffer.


### -param RequiredSize [out, optional]

A pointer to a variable to receive the number of characters required to store the friendly name (including a NULL terminator). This parameter is optional and can be <b>NULL</b>.


### -param MachineName [in, optional]

A pointer to NULL-terminated string that contains the name of a remote computer on which the hardware profile ID resides. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, the hardware profile ID is on the local computer. 


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilefriendlynamea">SetupDiGetHwProfileFriendlyName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelistexa">SetupDiGetHwProfileListEx</a>
 

 

