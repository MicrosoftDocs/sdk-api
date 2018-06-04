---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _WTSCONFIGINFOA structure


## -description


Contains information about a Remote Desktop Services session.  This structure is returned by the <a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a> function when you specify "WTSConfigInfo" for the <i>WTSInfoClass</i> parameter. 


## -struct-fields




### -field version

This member is reserved.


### -field fConnectClientDrivesAtLogon

This member is reserved.


### -field fConnectPrinterAtLogon

This member is reserved.


### -field fDisablePrinterRedirection

Specifies whether the client can use printer redirection.



#### 0

Enable client printer redirection.



#### 1

Disable client printer redirection.


### -field fDisableDefaultMainClientPrinter

Specifies whether the printer connected to the client is the default printer for the user.



#### 0

The printer connected to the client is not the default printer for the user.



#### 1

The printer connected to the client is the default printer for the user.


### -field ShadowSettings

The remote control setting. Remote control allows a user to remotely monitor the on-screen operations of another user. This member can be one of the following values.



#### 0

Remote control is disabled.



#### 1

The user of remote control has full control of the user's session, with the user's permission.



#### 2

The user of remote control has full control of the user's session; the user's permission is 
        not required.



#### 3

The user of remote control can view the session remotely, with the user's permission; the remote user 
        cannot actively control the session.



#### 4

The user of remote control can view the session remotely but not actively control the session; the 
        user's permission is not required.


### -field LogonUserName

A null-terminated string that contains the user name used in automatic logon scenarios.


### -field LogonDomain

A null-terminated string that contains the domain name used in automatic logon scenarios.


### -field WorkDirectory

A null-terminated string that contains the path of the working directory of  the initial program.


### -field InitialProgram

A null-terminated string that contains the name of  the program to start immediately after the user logs on to the server.


### -field ApplicationName

This member is reserved.


## -see-also




<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>
 

 

