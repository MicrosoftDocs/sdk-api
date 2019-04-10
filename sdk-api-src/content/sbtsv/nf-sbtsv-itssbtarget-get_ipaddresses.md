---
UID: NF:sbtsv.ITsSbTarget.get_IpAddresses
title: ITsSbTarget::get_IpAddresses (sbtsv.h)
author: windows-sdk-content
description: Retrieves or specifies the external IP addresses of the target.
old-location: termserv\itssbtarget_ipaddresses.htm
tech.root: TermServ
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbTarget interface [Remote Desktop Services],IpAddresses property, ITsSbTarget.IpAddresses, ITsSbTarget.TargetExternalIpAddresses, ITsSbTarget.get_IpAddresses, ITsSbTarget::IpAddresses, ITsSbTarget::get_IpAddresses, ITsSbTarget::get_TargetExternalIpAddresses, ITsSbTarget::put_IpAddresses, ITsSbTarget::put_TargetExternalIpAddresses, ITsSbTargetEx interface [Remote Desktop Services],IpAddresses property, ITsSbTargetEx.IpAddresses, ITsSbTargetEx::get_IpAddresses, ITsSbTargetEx::put_IpAddresses, IpAddresses property [Remote Desktop Services], IpAddresses property [Remote Desktop Services],ITsSbTarget interface, IpAddresses property [Remote Desktop Services],ITsSbTargetEx interface, TargetExternalIpAddresses, TargetExternalIpAddresses property [Remote Desktop Services], TargetExternalIpAddresses property [Remote Desktop Services],ITsSbTarget interface, get_IpAddresses, sbtsv/ITsSbTarget::IpAddresses, sbtsv/ITsSbTarget::get_IpAddresses, sbtsv/ITsSbTarget::put_IpAddresses, sbtsv/ITsSbTargetEx::IpAddresses, sbtsv/ITsSbTargetEx::get_IpAddresses, sbtsv/ITsSbTargetEx::put_IpAddresses, termserv.itssbtarget_ipaddresses
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbTarget.IpAddresses
 - ITsSbTarget.get_IpAddresses
 - ITsSbTarget.put_IpAddresses
 - ITsSbTargetEx.IpAddresses
 - ITsSbTargetEx.get_IpAddresses
 - ITsSbTargetEx.put_IpAddresses
 - TargetExternalIpAddresses
 - ITsSbTarget.TargetExternalIpAddresses
 - ITsSbTarget::get_TargetExternalIpAddresses
 - ITsSbTarget::put_TargetExternalIpAddresses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbTarget::get_IpAddresses


## -description


 Retrieves or specifies the external IP addresses of the target.

This property is read/write.


## -parameters


## -remarks



This property was formerly known as <b>TargetExternalIpAddresses</b> in Windows Server 2008 R2.

If the number of external IP addresses is unknown, you can call this method with <i>sockaddr</i> set to <b>NULL</b>. The method will then return, in the <i>numAddresses</i> parameter, the number of <a href="https://msdn.microsoft.com/en-us/library/Ee351748(v=VS.85).aspx">TSSD_ConnectionPoint</a> structures necessary to receive all the external IP addresses. Allocate the array for <i>sockaddr</i> based on this number, and then call the method again, setting <i>sockaddr</i> to the newly allocated array and <i>numAddresses</i> to the number returned by the first call.




## -see-also




<a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>



<a href="https://msdn.microsoft.com/3f0f26fb-e8bc-47eb-8038-e51792ad4376">ITsSbTargetEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee351748(v=VS.85).aspx">TSSD_ConnectionPoint</a>
 

 

