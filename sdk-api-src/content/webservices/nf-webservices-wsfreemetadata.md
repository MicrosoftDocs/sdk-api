---
UID: NF:webservices.WsFreeMetadata
title: WsFreeMetadata function (webservices.h)
author: windows-sdk-content
description: Releases the memory resource associated with a metadata object.
old-location: wsw\wsfreemetadata.htm
tech.root: wsw
ms.assetid: 4e159619-3807-4e7f-9198-fb74962ae141
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsFreeMetadata, WsFreeMetadata function [Web Services for Windows], webservices/WsFreeMetadata, wsw.wsfreemetadata
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsFreeMetadata function


## -description


Releases the memory resource associated with a metadata object.
            


## -parameters




### -param metadata [in]

A pointer to the metadata object to release.  The pointer must reference a valid <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-metadata">WS_METADATA</a> object returned
                    by <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wscreatemetadata">WsCreateMetadata</a> and the referenced value may not be <b>NULL</b>.
                


## -returns



This function does not return a value.




## -remarks



Any <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-policy">WS_POLICY</a> objects that
                were retrieved using the metadata object will also be freed.
            



