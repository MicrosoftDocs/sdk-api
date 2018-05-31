---
UID: NF:amparse.IAMParse.SetParseTime
title: IAMParse::SetParseTime
author: windows-sdk-content
description: The SetParseTime method sets the current stream parse time. For MPEG-2, this corresponds to the system clock time computed for the current stream position.
old-location: dshow\iamparse_setparsetime.htm
old-project: DirectShow
ms.assetid: 52c53994-7cb7-4f50-a00d-87faa309c717
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMParse interface [DirectShow],SetParseTime method, IAMParse.SetParseTime, IAMParse::SetParseTime, IAMParseSetParseTime, SetParseTime, SetParseTime method [DirectShow], SetParseTime method [DirectShow],IAMParse interface, amparse/IAMParse::SetParseTime, dshow.iamparse_setparsetime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amparse.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SOCKADDR_IRDA, *PSOCKADDR_IRDA, *LPSOCKADDR_IRDA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMParse.SetParseTime
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IAMParse::SetParseTime


## -description



The <code>SetParseTime</code> method sets the current stream parse time. For MPEG-2, this corresponds to the system clock time computed for the current stream position.




## -parameters




### -param rtCurrent






#### - rtPosition [in]

Current stream parse time.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The parse time is not available, because the input pin is not connected

</td>
</tr>
</table>
 




## -remarks



The parse time for the MPEG-2 Splitter filter is the current stream position in system clock units. The initial value of the parse time is zero.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c5f3e153-c92f-4cdf-9aae-336b1f3dd8d6">IAMParse Interface</a>
 

 

