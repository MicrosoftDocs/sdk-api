---
UID: NN:faxcomex.IFaxLoggingOptions
title: IFaxLoggingOptions
author: windows-sdk-content
description: The IFaxLoggingOptions interface is used by a fax client application to access and configure the event logging categories and the activity logging options that the fax service is using.
old-location: fax\_mfax_faxloggingoptions_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_70c3_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxLoggingOptions, IFaxLoggingOptions interface [Fax Service], IFaxLoggingOptions interface [Fax Service],described, _mfax_faxloggingoptions_cpp, fax._mfax_faxloggingoptions_cpp, faxcomex/IFaxLoggingOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxLoggingOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxLoggingOptions interface


## -description


The <b>IFaxLoggingOptions</b> interface is used by a fax client application to access and configure the event logging categories and the activity logging options that the fax service is using.

The <b>IFaxLoggingOptions</b> interface is accessed through an <a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a> interface. It provides access to the <a href="https://msdn.microsoft.com/225afdb8-7249-4aa5-bbde-638adf02eb41">FaxActivityLogging</a> and <a href="https://msdn.microsoft.com/c46f1b55-8211-4c9b-a622-356f2ea2db36">FaxEventLogging</a> methods. 


## -remarks



To create a <b>FaxLoggingOptions</b> object in C++, call the <a href="https://msdn.microsoft.com/51abefd8-e8b2-42f8-a4dc-f2aa8ffc9ef6">LoggingOptions</a> method.




## -see-also




<a href="https://msdn.microsoft.com/438e4e89-88c9-431d-b774-98e65cf57064">FaxLoggingOptions</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>
 

 

