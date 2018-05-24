---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
title: D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
author: windows-driver-content
description: Contains the response to a D3D11_AUTHENTICATED_QUERY_PROTECTION query.
old-location: mf\d3d11_authenticated_query_protection_output.htm
old-project: medfound
ms.assetid: F70D5AFC-06A6-408D-A951-1280FBBF8E89
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT, D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT, mf.d3d11_authenticated_query_protection_output
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11.h
api_name:
-	D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT structure


## -description


Contains the response to a <b>D3D11_AUTHENTICATED_QUERY_PROTECTION</b> query.




## -struct-fields




### -field Output

A <a href="https://msdn.microsoft.com/D5650992-04D0-4DD2-A858-1E7FB979A9C2">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.




### -field ProtectionFlags

A <a href="https://msdn.microsoft.com/037AB541-2E68-460C-8626-7F22C6C3E425">D3D11_AUTHENTICATED_PROTECTION_FLAGS</a> union that specifies the protection level.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

