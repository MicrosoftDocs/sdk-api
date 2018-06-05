---
UID: NF:webservices.WsSetReaderPosition
title: WsSetReaderPosition function
author: windows-sdk-content
description: Sets the current position of the Reader. The position must have been obtained by a call to WsGetReaderPosition or WsGetWriterPosition. This function can only be used on a reader that is set to a WS_XML_BUFFER.
old-location: wsw\wssetreaderposition.htm
old-project: wsw
ms.assetid: cc879cc0-c8ca-457e-9ff1-ae220e31cb04
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsSetReaderPosition, WsSetReaderPosition function [Web Services for Windows], webservices/WsSetReaderPosition, wsw.wssetreaderposition
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsSetReaderPosition
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsSetReaderPosition function


## -description


Sets the current position of the Reader.  The position must have been obtained by a call to
        <a href="https://msdn.microsoft.com/91e543f3-7325-4a90-9b99-c98918478853">WsGetReaderPosition</a> or <a href="https://msdn.microsoft.com/0c0fbd78-ed4f-40da-a63d-a2f38136ecb3">WsGetWriterPosition</a>.
      
        This function can only be used on a reader that is set to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>.
      


## -parameters




### -param reader [in]

A pointer to the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object for which the current position is set.  The pointer must reference a valid <b>XML Reader</b> object.
                


### -param nodePosition [in]

A pointer to the position to set the Reader.
        


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

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

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>
 




## -remarks






        See <a href="https://msdn.microsoft.com/40ca058c-04e1-4358-b330-360a094a8791">WS_XML_NODE_POSITION</a> for more information on using positions.
      


        This function cannot be used while canonicalizing.  If <a href="https://msdn.microsoft.com/5dad9485-db3c-4ae0-b053-e1e4f32ad64d">WsStartReaderCanonicalization</a> has
        been called, then it will return <b>WS_E_INVALID_OPERATION</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)



