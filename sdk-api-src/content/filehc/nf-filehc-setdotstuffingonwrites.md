---
UID: NF:filehc.SetDotStuffingOnWrites
title: SetDotStuffingOnWrites function
author: windows-sdk-content
description: Enables dot-stuffing properties on the write path of the file handle cache of the message.
old-location: winprog\_setdotstuffingonwrites.htm
tech.root: DevNotes
ms.assetid: 6191e097-3e8a-4149-85bb-88d804caa3ae
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetDotStuffingOnWrites, SetDotStuffingOnWrites function [Windows API], filehc/SetDotStuffingOnWrites, winprog._setdotstuffingonwrites
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: filehc.h
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
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - SetDotStuffingOnWrites
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetDotStuffingOnWrites function


## -description


Enables dot-stuffing properties on the write path of the file handle cache of the message.


## -parameters




### -param pContext [in]

A pointer to an <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that contains context information.


### -param fEnable [in]

Specifies whether dot stuffing is available. If <b>FALSE</b>, all dot-stuffing behavior is turned off.


### -param fStripDots [in]

Specifies whether occurrences of "\r\n." are converted to "\r\n" within the message. If <b>TRUE</b>,  "\r\n." is converted to "\r\n" (unstuffing or stripping). If  <b>FALSE</b>,   "\r\n." is converted to "\r\n.." (stuffing).


## -returns



Returns <b>TRUE</b> if the function succeeds; otherwise, it is <b>FALSE</b>.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

