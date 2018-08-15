---
UID: NF:mi.MI_Instance_Normalize
title: MI_Instance_Normalize function
author: windows-sdk-content
description: Parses an MI_Instance_ExFT structure and then retrieves the MI_InstanceFT function table.
old-location: wmi_v2\mi_instance_normalize.htm
old-project: wmi_v2
ms.assetid: 4FE8FD63-78F4-41C8-9A72-A2E3ABDEBB86
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Instance_Normalize, MI_Instance_Normalize function [Windows Management Infrastructure (MI)], mi/MI_Instance_Normalize, wmi_v2.mi_instance_normalize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mi.h
api_name:
 - MI_Instance_Normalize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Instance_Normalize function


## -description


Parses an <a href="https://msdn.microsoft.com/E703D978-7B4B-4AB4-AB69-C9489F5AD58B">MI_Instance_ExFT</a> structure and 
    then retrieves  the <a href="https://msdn.microsoft.com/a8cd93b7-c9e0-415e-811a-33826e38417f">MI_InstanceFT</a> function 
    table.


## -parameters




### -param self [in, out]

A pointer to the object that receives the function table.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/9B9C2BEF-02E8-4C7D-96DB-236BF6F9B1F9">MI Interfaces</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>



<a href="https://msdn.microsoft.com/a8cd93b7-c9e0-415e-811a-33826e38417f">MI_InstanceFT</a>
 

 

