---
UID: NF:ole2.OleQueryLinkFromData
title: OleQueryLinkFromData function (ole2.h)
author: windows-sdk-content
description: Determines whether an OLE linked object (rather than an OLE embedded object) can be created from a clipboard data object.
old-location: com\olequerylinkfromdata.htm
tech.root: com
ms.assetid: 9ebdcd7f-06c1-4464-a66c-4d134a6b5d36
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OleQueryLinkFromData, OleQueryLinkFromData function [COM], _ole_OleQueryLinkFromData, com.olequerylinkfromdata, ole2/OleQueryLinkFromData
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
 - Ext-MS-Win-Com-OLE32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleQueryLinkFromData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleQueryLinkFromData function


## -description


Determines whether an OLE linked object (rather than an OLE embedded object) can be created from a clipboard data object.




## -parameters




### -param pSrcDataObject [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the clipboard data object from which the object is to be created.


## -returns



Returns S_OK if the <a href="https://msdn.microsoft.com/3eda0cf5-c33d-43cf-ba8a-02a4f6383adc">OleCreateLinkFromData</a> function can be used to create the linked object; otherwise S_FALSE.




## -remarks



The <b>OleQueryLinkFromData</b> function is similar to the <a href="https://msdn.microsoft.com/58fffb8c-9726-4801-84ce-6fb670b865c8">OleQueryCreateFromData</a> function, but determines whether an OLE linked object (rather than an OLE embedded object) can be created from the clipboard data object. If the return value is S_OK, the application can then attempt to create the object with a call to <a href="https://msdn.microsoft.com/3eda0cf5-c33d-43cf-ba8a-02a4f6383adc">OleCreateLinkFromData</a>. A successful return from <b>OleQueryLinkFromData</b> does not, however, guarantee the successful creation of a link.




