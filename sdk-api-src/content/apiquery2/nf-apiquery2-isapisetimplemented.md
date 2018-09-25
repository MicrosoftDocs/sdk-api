---
UID: NF:apiquery2.IsApiSetImplemented
title: IsApiSetImplemented function
author: windows-sdk-content
description: The IsApiSetImplemented function tests if a specified API set is present on the computer.
old-location: winprog\isapisetimplemented.htm
tech.root: devnotes
ms.assetid: DF177716-9F33-4E39-BD63-D1B8E39CD67C
ms.author: windowssdkdev
ms.date: 09/21/2018
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


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>IsApiSetImplemented</b> function tests if a specified API set is present on the computer.


## -parameters




### -param Contract

Specifies the name of the API set to query.


## -returns



<b>IsApiSetImplemented</b> returns <b>TRUE</b> if the specified API set is present. In this case, APIs in the target API set have valid implementations on the current
 platform.

Otherwise, this function returns <b>FALSE</b>.




## -remarks



When writing code that targets OneCore platforms, you can only call the subset of APIs that is available on OneCore. If your code calls APIs that are not available on OneCore, you may see ApiValidator errors during compilation, and then at runtime your code may not behave as expected.





   To fix this problem, you can wrap the API call in <b>IsApiSetImplemented</b>. For more information and examples of usage, see <a href="https://docs.microsoft.com/windows-hardware/drivers/develop/building-for-onecore">Building for OneCore</a>.

By making use of <b>IsApiSetImplemented</b>, you can target OneCore and Desktop systems with a single binary.


 


You don't need to call <b>IsApiSetImplemented</b> for universal APIs because they are by definition present on both OneCore and Desktop versions of Windows.

 See the corresponding API reference documentation pages to determine if a given API is universally available. Look for the <b>Target Platform</b> line in the requirements block of the documentation page.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/develop/building-for-onecore">Building for OneCore</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/develop/validating-universal-drivers">Validating Universal Windows drivers</a>
 

 

