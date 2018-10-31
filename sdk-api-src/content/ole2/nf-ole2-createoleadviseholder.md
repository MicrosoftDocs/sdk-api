---
UID: NF:ole2.CreateOleAdviseHolder
title: CreateOleAdviseHolder function
author: windows-sdk-content
description: Creates an advise holder object for managing compound document notifications. It returns a pointer to the object's OLE implementation of the IOleAdviseHolder interface.
old-location: com\createoleadviseholder.htm
tech.root: com
ms.assetid: f76e074e-6814-4735-9417-d5970e73089f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateOleAdviseHolder, CreateOleAdviseHolder function [COM], _ole_CreateOleAdviseHolder, com.createoleadviseholder, ole2/CreateOleAdviseHolder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - CreateOleAdviseHolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateOleAdviseHolder function


## -description


Creates an advise holder object for managing compound document notifications. It returns a pointer to the object's OLE implementation of the <a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a> interface.


## -parameters




### -param ppOAHolder [out]

Address of <a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a> pointer variable that receives the interface pointer to the new advise holder object.


## -returns



This function returns S_OK on success and supports the standard return value E_OUTOFMEMORY.




## -remarks



The function <b>CreateOleAdviseHolder</b> creates an instance of an advise holder, which supports the OLE implementation of the <a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a> interface. The methods of this interface are intended to be used to implement the advisory methods of <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>, and, when advisory connections have been set up with objects supporting an advisory sink, to send notifications of changes in the object to the advisory sink. The advise holder returned by <b>CreateOleAdviseHolder</b> will suffice for the great majority of applications. The OLE-provided implementation does not, however, support <a href="https://msdn.microsoft.com/80a9ccd8-f89a-40c4-8b99-38536409cf26">IOleAdviseHolder::EnumAdvise</a>, so if you need to use this method, you will need to implement your own advise holder.





## -see-also




<a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>
 

 

