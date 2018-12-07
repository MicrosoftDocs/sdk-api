---
UID: NE:windef.DPI_HOSTING_BEHAVIOR
title: DPI_HOSTING_BEHAVIOR
author: windows-sdk-content
description: Identifies the DPI hosting behavior for a window. This behavior allows windows created in the thread to host child windows with a different DPI_AWARENESS_CONTEXT.
old-location: hidpi\_dpi_hosting_behavior.htm
tech.root: hidpi
ms.assetid: 4BFBF485-1AD2-4460-A4EE-CB76EF62B8C4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DPI_HOSTING_BEHAVIOR, DPI_HOSTING_BEHAVIOR_DEFAULT, DPI_HOSTING_BEHAVIOR_INVALID, DPI_HOSTING_BEHAVIOR_MIXED, _DPI_HOSTING_BEHAVIOR, _DPI_HOSTING_BEHAVIOR enumeration [High DPI], hidpi._dpi_hosting_behavior, windef/DPI_HOSTING_BEHAVIOR_DEFAULT, windef/DPI_HOSTING_BEHAVIOR_INVALID, windef/DPI_HOSTING_BEHAVIOR_MIXED, windef/_DPI_HOSTING_BEHAVIOR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: windef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - windef.h
api_name:
 - _DPI_HOSTING_BEHAVIOR
product: Windows
targetos: Windows
req.typenames: DPI_HOSTING_BEHAVIOR
req.redist: 
---

# DPI_HOSTING_BEHAVIOR enumeration


## -description


Identifies the DPI hosting behavior for a window. This behavior allows windows created in the thread to host child windows with a different <b>DPI_AWARENESS_CONTEXT</b>


## -enum-fields




### -field DPI_HOSTING_BEHAVIOR_INVALID

Invalid DPI hosting behavior. This usually occurs if the previous <a href="https://msdn.microsoft.com/CF31D96A-EC84-4911-81A2-82EC90D417B9">SetThreadDpiHostingBehavior</a> call used an invalid parameter.


### -field DPI_HOSTING_BEHAVIOR_DEFAULT

Default DPI hosting behavior. The associated window behaves as normal, and cannot create or re-parent child windows with a different <b>DPI_AWARENESS_CONTEXT</b>.


### -field DPI_HOSTING_BEHAVIOR_MIXED

Mixed DPI hosting behavior. This enables the creation and re-parenting of child windows with different <b>DPI_AWARENESS_CONTEXT</b>. These child windows will be independently scaled by the OS.


## -remarks



<b>DPI_HOSTING_BEHAVIOR</b> enables a mixed content hosting behavior, which allows parent windows created in the thread to host child windows with a different <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> value. This property only effects new windows created within this thread while the mixed hosting behavior is active. A parent window with this hosting behavior is able to host child windows with different <b>DPI_AWARENESS_CONTEXT</b> values, regardless of whether the child windows have mixed hosting behavior enabled.

This hosting behavior does not allow for windows with per-monitor <b>DPI_AWARENESS_CONTEXT</b> values to be hosted until windows with <b>DPI_AWARENESS_CONTEXT</b> values of system or unaware.

To avoid unexpected outcomes, a thread's <b>DPI_HOSTING_BEHAVIOR</b> should be changed to support mixed hosting behaviors only when creating a new window which needs to support those behaviors. Once that window is created, the hosting behavior should be switched back to its default value.

Enabling mixed hosting behavior will not automatically adjust the thread's <b>DPI_AWARENESS_CONTEXT</b> to be compatible with legacy content. The thread's awareness context must still be manually changed before new windows are created to host such content.






## -see-also




<a href="https://msdn.microsoft.com/B9500745-9B53-47FF-9F45-0BFF3A66FD46">GetThreadDpiHostingBehavior</a>



<a href="https://msdn.microsoft.com/BD16F545-54A1-479A-BA4B-F54834043EB2">GetWindowDpiHostingBehavior</a>



<a href="https://msdn.microsoft.com/CF31D96A-EC84-4911-81A2-82EC90D417B9">SetThreadDpiHostingBehavior</a>
 

 

