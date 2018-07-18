---
UID: NF:setupapi.SetupDiClassGuidsFromNameA
title: SetupDiClassGuidsFromNameA function
author: windows-sdk-content
description: The SetupDiClassGuidsFromName function retrieves the GUID(s) associated with the specified class name. This list is built based on the classes currently installed on the system.
old-location: devinst\setupdiclassguidsfromname.htm
old-project: devinst
ms.assetid: 54516c6f-ec78-47ea-93f5-a4c7cde5a601
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SetupDiClassGuidsFromName, SetupDiClassGuidsFromName function [Device and Driver Installation], SetupDiClassGuidsFromNameA, SetupDiClassGuidsFromNameW, devinst.setupdiclassguidsfromname, di-rtns_6b309545-3832-4802-9668-21a107f3c651.xml, setupapi/SetupDiClassGuidsFromName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiClassGuidsFromName
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupDiClassGuidsFromNameA function


## -description


The <b>SetupDiClassGuidsFromName</b> function retrieves the GUID(s) associated with the specified class name. This list is built based on the classes currently installed on the system.


## -parameters




### -param ClassName [in]

The name of the class for which to retrieve the class GUID.


### -param ClassGuidList [out]

A pointer to an array to receive the list of GUIDs associated with the specified class name.


### -param ClassGuidListSize [in]

The number of GUIDs in the <i>ClassGuidList</i> array.


### -param RequiredSize [out]

Supplies a pointer to a variable that receives the number of GUIDs associated with the class name. If this number is greater than the size of the <i>ClassGuidList</i> buffer, the number indicates how large the array must be in order to store all the GUIDs.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Call <b>SetupDiClassGuidsFromNameEx</b> to retrieve the class GUIDs for a class on a remote computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550941">SetupDiClassGuidsFromNameEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550947">SetupDiClassNameFromGuid</a>
 

 

