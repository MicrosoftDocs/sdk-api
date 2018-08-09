---
UID: NF:mmcobj.View.ExecuteShellCommand
title: View::ExecuteShellCommand
author: windows-sdk-content
description: The ExecuteShellCommand method runs a command in a window. After this method successfully starts the command in a separate process, it returns immediately (it does not wait for the command to complete).
old-location: mmc\view_executeshellcommand.htm
old-project: MMC
ms.assetid: e786df29-b9ad-4cdd-81b1-99fe73a551fb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ""Maximized", "Minimized", "Restored", ExecuteShellCommand, ExecuteShellCommand method [MMC], ExecuteShellCommand method [MMC],View interface, ExecuteShellCommand method [MMC],View object, View interface [MMC],ExecuteShellCommand method, View object [MMC],ExecuteShellCommand method, View.ExecuteShellCommand, View::ExecuteShellCommand, _slate_view.executeshellcommand_method, mmc.view_executeshellcommand"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MMCObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_PROPERTY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.exe
api_name:
 - View.ExecuteShellCommand
 - View.ExecuteShellCommand
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# View::ExecuteShellCommand


## -description


The 
<b>ExecuteShellCommand</b> method runs a command in a window. After this method successfully starts the command in a separate process, it returns immediately (it does not wait for the command to complete).


## -parameters




### -param Command

A value that specifies the command to execute. A fully qualified path may be specified. Any environment variables (such as "%windir%") contained in <i>Command</i> will be expanded.


### -param Directory

A value that specifies the name of the working directory. Any environment variables contained in <i>Directory</i> will be expanded. If <i>Directory</i> is an empty string, the current directory is used as the working directory.


### -param Parameters

A value that specifies parameters, if any, to be used by <i>Command</i>; the parameters must be separated by spaces. For example, specifying <i>Parameters</i> as "Param1 Param2" results in <i>Command</i> receiving Param1 and Param2 as parameters. If an individual parameter is required to be in double quotation marks, use the proper technique for your programming language. For example, in Microsoft Visual Basic, specifying <i>Parameters</i> as "Param1 ""This is Param2""" results in <i>Command</i> receiving Param1 and "This is Param2" as parameters.


### -param WindowState

A value that specifies the state for the window. This value can be one of the following string values or an empty string. If it's an empty string, it defaults to "Restored".



#### "Maximized"

The command executes in a maximized window.



#### "Minimized"

The command executes in a minimized window.



#### "Restored"

The command executes in a restored, or normal, window.


## -returns



This method does not return a value.



