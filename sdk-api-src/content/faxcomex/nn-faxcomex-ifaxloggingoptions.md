---
UID: NN:faxcomex.IFaxLoggingOptions
title: IFaxLoggingOptions
author: windows-sdk-content
description: The IFaxLoggingOptions interface is used by a fax client application to access and configure the event logging categories and the activity logging options that the fax service is using.
old-location: fax\_mfax_faxloggingoptions_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_70c3_cpp.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
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

The <b>IFaxLoggingOptions</b> interface is accessed through an <a href="https://msdn.microsoft.com/en-us/library/ms689110(v=VS.85).aspx">IFaxServer</a> interface. It provides access to the <a href="https://msdn.microsoft.com/en-us/library/ms684576(v=VS.85).aspx">FaxActivityLogging</a> and <a href="https://msdn.microsoft.com/en-us/library/ms684912(v=VS.85).aspx">FaxEventLogging</a> methods. 


## -remarks



To create a <b>FaxLoggingOptions</b> object in C++, call the <a href="https://msdn.microsoft.com/en-us/library/ms690044(v=VS.85).aspx">LoggingOptions</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686863(v=VS.85).aspx">FaxLoggingOptions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689110(v=VS.85).aspx">IFaxServer</a>
 

 

