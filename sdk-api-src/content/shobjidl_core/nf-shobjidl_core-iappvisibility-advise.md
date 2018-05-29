---
UID: NF:shobjidl_core.IAppVisibility.Advise
title: IAppVisibility::Advise
author: windows-sdk-content
description: Registers an advise sink object to receive notification of changes to the display.
old-location: shell\IAppVisibility_Advise.htm
old-project: shell
ms.assetid: 602F46EF-014C-4219-9C1F-C1B4371EA456
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IAppVisibility interface, IAppVisibility interface [Windows Shell],Advise method, IAppVisibility.Advise, IAppVisibility::Advise, shell.IAppVisibility_Advise, shobjidl_core/IAppVisibility::Advise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IAppVisibility.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAppVisibility::Advise


## -description


Registers an advise sink object to receive notification of changes to the display.


## -parameters




### -param pCallback [in]

The client's advise sink that receives outgoing calls from the connection point.


### -param pdwCookie [out]

A token that uniquely identifies this connection. Use this token to delete the connection by passing it to the <a href="https://msdn.microsoft.com/D670F1E7-5E0B-498E-8F27-DF2A3A387862">Unadvise</a> method.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwCookie</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/89E26D36-3536-45F5-9396-83CCFB26890B">IAppVisibility</a>



<a href="https://msdn.microsoft.com/F6BABF7D-FA05-4A68-878F-A27A6990EC3F">IAppVisibilityEvents</a>
 

 

