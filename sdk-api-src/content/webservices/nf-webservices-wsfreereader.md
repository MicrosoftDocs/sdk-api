---
UID: NF:webservices.WsFreeReader
title: WsFreeReader function
author: windows-sdk-content
description: Releases the memory resource associated with an XML_Reader object.
old-location: wsw\wsfreereader.htm
old-project: wsw
ms.assetid: 31163bea-266f-43a3-bdf5-61386ebc197c
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsFreeReader, WsFreeReader function [Web Services for Windows], webservices/WsFreeReader, wsw.wsfreereader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
 - WsFreeReader
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsFreeReader function


## -description


Releases the memory resource associated with  an XML_Reader object.
            


## -parameters




### -param reader [in]


          
                    
                    A pointer to the <b>XML Reader</b> object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object returned by <a href="https://msdn.microsoft.com/0d4449aa-ffcc-41d9-99b1-7352edaf3700">WsCreateReader</a>    and the referenced <b>XML Reader</b> value may not be <b>NULL</b>.
        


## -returns



This function does not return a value.



