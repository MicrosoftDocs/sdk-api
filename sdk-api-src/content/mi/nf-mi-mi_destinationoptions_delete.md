---
UID: NF:mi.MI_DestinationOptions_Delete
title: MI_DestinationOptions_Delete function
author: windows-driver-content
description: Deletes the destination options structure created by using the MI_Application_NewDestinationOptions or MI_DestinationOptions_Clone function.
old-location: wmi_v2\mi_destinationoptions_delete.htm
old-project: wmi_v2
ms.assetid: c4cc8622-1adb-4e91-877f-11a260ca4bd7
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_DestinationOptions_Delete, MI_DestinationOptions_Delete function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_Delete, wmi_v2.mi_destinationoptions_delete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
req.include-header: 
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_DestinationOptions_Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_Delete function


## -description


Deletes the destination options structure created by using the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> or <a href="https://msdn.microsoft.com/f331561b-97ad-42f1-91b3-d180db92da07">MI_DestinationOptions_Clone</a> function.


## -parameters




### -param options [in, out]

A pointer to the destination options structure to delete.

