---
UID: NF:webservices.WsFreeMetadata
title: WsFreeMetadata function
author: windows-sdk-content
description: Releases the memory resource associated with a metadata object.
old-location: wsw\wsfreemetadata.htm
old-project: wsw
ms.assetid: 4e159619-3807-4e7f-9198-fb74962ae141
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsFreeMetadata, WsFreeMetadata function [Web Services for Windows], webservices/WsFreeMetadata, wsw.wsfreemetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsFreeMetadata
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsFreeMetadata function


## -description


Releases the memory resource associated with a metadata object.
            


## -parameters




### -param metadata [in]

A pointer to the metadata object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/aa7383a1-60fa-448a-b0c6-b9c49d9d5070">WS_METADATA</a> object returned
                    by <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a> and the referenced value may not be <b>NULL</b>.
                


## -returns



This function does not return a value.




## -remarks



Any <a href="https://msdn.microsoft.com/04623686-5065-4e97-8685-c72f848b92ab">WS_POLICY</a> objects that
                were retrieved using the metadata object will also be freed.
            



