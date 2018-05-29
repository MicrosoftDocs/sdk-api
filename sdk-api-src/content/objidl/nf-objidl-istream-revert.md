---
UID: NF:objidl.IStream.Revert
title: IStream::Revert
author: windows-sdk-content
description: The Revert method discards all changes that have been made to a transacted stream since the last IStream::Commit call. On streams open in direct mode and streams using the COM compound file implementation of IStream::Revert, this method has no effect.
old-location: stg\istream_revert.htm
old-project: Stg
ms.assetid: 1a707b17-840f-4cd2-9e43-97a8c02120b8
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IStream interface [Structured Storage],Revert method, IStream.Revert, IStream::Revert, Revert, Revert method [Structured Storage], Revert method [Structured Storage],IStream interface, _stg_istream_revert, objidl/IStream::Revert, stg.istream_revert
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IStream.Revert
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStream::Revert


## -description


The <b>Revert</b> method discards all changes that have been made to a transacted stream since the last 
<a href="https://msdn.microsoft.com/335c3a53-ca6a-42f3-bbf9-684ed48591e6">IStream::Commit</a> call. On streams open in direct mode and streams using the COM compound file implementation of <b>IStream::Revert</b>, this method has no effect.


## -parameters






## -returns



This method can return one of these values.




## -remarks



The <b>Revert</b> method discards changes made to a transacted stream since the last commit operation.




## -see-also




<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/335c3a53-ca6a-42f3-bbf9-684ed48591e6">IStream::Commit</a>
 

 

