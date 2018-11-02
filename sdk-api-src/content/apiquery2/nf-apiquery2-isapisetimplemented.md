---
UID: NF:apiquery2.IsApiSetImplemented
title: IsApiSetImplemented function
author: windows-sdk-content
description: The IsApiSetImplemented function tests if a specified API set is present on the computer.
old-location: winprog\isapisetimplemented.htm
tech.root: devnotes
ms.assetid: DF177716-9F33-4E39-BD63-D1B8E39CD67C
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IsApiSetImplemented, IsApiSetImplemented function [Windows API], apiquery2/IsApiSetImplemented, winprog.isapisetimplemented
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: apiquery2.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - apiquery2.h
api_name:
 - IsApiSetImplemented
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsApiSetImplemented function


## -description


The <b>IsApiSetImplemented</b> function tests if a specified API set is present on the computer.


## -parameters




### -param Contract

Specifies the name of the API set to query.  For more info, see the Remarks section.


## -returns



<b>IsApiSetImplemented</b> returns <b>TRUE</b> if the specified API set is present. In this case, APIs in the target API set have valid implementations on the current
 platform.

Otherwise, this function returns <b>FALSE</b>.




## -remarks



On OneCore, APIs are organized into functional groups called API sets. Depending on applicability, a given API set may be unavailable on the target platform.

When writing code that targets OneCore and Desktop platforms,  you may see ApiValidator errors during compilation if your code calls APIs from API sets not present on the computer.

To fix this problem, wrap the API call in <b>IsApiSetImplemented</b>.  This function tests at runtime if the specified API set is present on the target platform.

To determine the API set for a given API, find the API name on the <a href="https://docs.microsoft.com/windows/desktop/apiindex/umbrella-lib-onecoreuap">OneCoreUap umbrella library</a> page and remove the <code>.dll</code> suffix from the requirements entry.

By making use of <b>IsApiSetImplemented</b>, you can target OneCore and Desktop systems with a single binary.


 


You don't need to call <b>IsApiSetImplemented</b> for universal APIs because they are by definition present on both OneCore and Desktop versions of Windows.

 See the corresponding API reference documentation pages to determine if a given API is universally available. Look for the <b>Target Platform</b> line in the requirements block of the documentation page.

 For more information and examples of usage, see <a href="https://docs.microsoft.com/windows-hardware/drivers/develop/building-for-onecore">Building for OneCore</a>.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/develop/building-for-onecore">Building for OneCore</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/develop/validating-universal-drivers">Validating Universal Windows drivers</a>
 

 

