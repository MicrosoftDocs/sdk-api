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

# __MIDL___MIDL_itf_msctf_0000_0070_0002 enumeration


## -description


Elements of the <b>TF_DA_COLORTYPE</b> enumeration specify the format of the color contained in the <a href="https://msdn.microsoft.com/0ce8f941-c187-437f-8bad-f882e63b8421">TF_DA_COLOR</a> structure.


## -enum-fields




### -field TF_CT_NONE

The structure contains no color data.


### -field TF_CT_SYSCOLOR

The color is specified as a system color index. For more information about the system color indexes, see <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>.


### -field TF_CT_COLORREF

The color is specified as an RGB value.


## -see-also




<a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>



<a href="https://msdn.microsoft.com/0ce8f941-c187-437f-8bad-f882e63b8421">TF_DA_COLOR
      </a>
 

 

