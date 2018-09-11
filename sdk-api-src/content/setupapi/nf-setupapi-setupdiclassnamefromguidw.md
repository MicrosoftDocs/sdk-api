---
UID: NF:setupapi.SetupDiClassNameFromGuidW
title: SetupDiClassNameFromGuidW function
author: windows-sdk-content
description: The SetupDiClassNameFromGuid function retrieves the class name associated with a class GUID.
old-location: devinst\setupdiclassnamefromguid.htm
tech.root: devinst
ms.assetid: e23631b4-eb7f-4a75-ac23-25d3d974a3e3
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SetupDiClassNameFromGuid, SetupDiClassNameFromGuid function [Device and Driver Installation], SetupDiClassNameFromGuidA, SetupDiClassNameFromGuidW, devinst.setupdiclassnamefromguid, di-rtns_b17476f2-25e2-48ed-be4d-53af55541056.xml, setupapi/SetupDiClassNameFromGuid
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
 - SetupDiClassNameFromGuid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiClassNameFromGuidW function


## -description


The <b>SetupDiClassNameFromGuid</b> function retrieves the class name associated with a class GUID.


## -parameters




### -param ClassGuid [in]

A pointer to the class GUID for the class name to retrieve.


### -param ClassName [out]

A pointer to a buffer that receives the NULL-terminated string that contains the name of the class that is specified by the pointer in the <i>ClassGuid</i> parameter.


### -param ClassNameSize [in]

The size, in characters, of the buffer that is pointed to by the <i>ClassName</i> parameter. The maximum size, in characters, of a NULL-terminated class name is MAX_CLASS_NAME_LEN. For more information about the class name size, see the following <b>Remarks</b> section.


### -param RequiredSize [out, optional]

A pointer to a variable that receives the number of characters that are required to store the requested NULL-terminated class name. This pointer is optional and can be <b>NULL</b>. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Call <b>SetupDiClassNameFromGuidEx</b> to retrieve the name for a class on a remote computer.

<b>SetupDiClassNameFromGuid</b> does not enforce a restriction on the length of the class name that it can return. This function returns the required size for a NULL-terminated class name even if it is greater than MAX_CLASS_NAME_LEN. However, MAX_CLASS_NAME_LEN is the maximum length of a valid NULL-terminated class name. A caller should never need a buffer that is larger than MAX_CLASS_NAME_LEN. For more information about class names, see the description of the <b>Class</b> entry of an <a href="https://msdn.microsoft.com/53e30950-28a3-4ae3-a351-a917b02c84a5">INF Version section</a>.




## -see-also




<a href="https://msdn.microsoft.com/54516c6f-ec78-47ea-93f5-a4c7cde5a601">SetupDiClassGuidsFromName</a>



<a href="https://msdn.microsoft.com/0d576df1-e259-4025-8ef0-a520f5680fa0">SetupDiClassNameFromGuidEx</a>
 

 

