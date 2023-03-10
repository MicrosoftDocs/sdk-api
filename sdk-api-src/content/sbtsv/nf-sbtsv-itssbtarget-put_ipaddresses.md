---
UID: NF:sbtsv.ITsSbTarget.put_IpAddresses
title: ITsSbTarget::put_IpAddresses (sbtsv.h)
description: Retrieves or specifies the external IP addresses of the target. (ITsSbTargetEx.put_IpAddresses)
helpviewer_keywords: ["ITsSbTarget interface [Remote Desktop Services]","IpAddresses property","ITsSbTarget.IpAddresses","ITsSbTarget.TargetExternalIpAddresses","ITsSbTarget.put_IpAddresses","ITsSbTarget::IpAddresses","ITsSbTarget::get_IpAddresses","ITsSbTarget::get_TargetExternalIpAddresses","ITsSbTarget::put_IpAddresses","ITsSbTarget::put_TargetExternalIpAddresses","ITsSbTargetEx interface [Remote Desktop Services]","IpAddresses property","ITsSbTargetEx.IpAddresses","ITsSbTargetEx::get_IpAddresses","ITsSbTargetEx::put_IpAddresses","IpAddresses property [Remote Desktop Services]","IpAddresses property [Remote Desktop Services]","ITsSbTarget interface","IpAddresses property [Remote Desktop Services]","ITsSbTargetEx interface","TargetExternalIpAddresses","TargetExternalIpAddresses property [Remote Desktop Services]","TargetExternalIpAddresses property [Remote Desktop Services]","ITsSbTarget interface","put_IpAddresses","sbtsv/ITsSbTarget::IpAddresses","sbtsv/ITsSbTarget::get_IpAddresses","sbtsv/ITsSbTarget::put_IpAddresses","sbtsv/ITsSbTargetEx::IpAddresses","sbtsv/ITsSbTargetEx::get_IpAddresses","sbtsv/ITsSbTargetEx::put_IpAddresses","termserv.itssbtarget_ipaddresses"]
old-location: termserv\itssbtarget_ipaddresses.htm
tech.root: TermServ
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.date: 12/05/2018
ms.keywords: ITsSbTarget interface [Remote Desktop Services],IpAddresses property, ITsSbTarget.IpAddresses, ITsSbTarget.TargetExternalIpAddresses, ITsSbTarget.put_IpAddresses, ITsSbTarget::IpAddresses, ITsSbTarget::get_IpAddresses, ITsSbTarget::get_TargetExternalIpAddresses, ITsSbTarget::put_IpAddresses, ITsSbTarget::put_TargetExternalIpAddresses, ITsSbTargetEx interface [Remote Desktop Services],IpAddresses property, ITsSbTargetEx.IpAddresses, ITsSbTargetEx::get_IpAddresses, ITsSbTargetEx::put_IpAddresses, IpAddresses property [Remote Desktop Services], IpAddresses property [Remote Desktop Services],ITsSbTarget interface, IpAddresses property [Remote Desktop Services],ITsSbTargetEx interface, TargetExternalIpAddresses, TargetExternalIpAddresses property [Remote Desktop Services], TargetExternalIpAddresses property [Remote Desktop Services],ITsSbTarget interface, put_IpAddresses, sbtsv/ITsSbTarget::IpAddresses, sbtsv/ITsSbTarget::get_IpAddresses, sbtsv/ITsSbTarget::put_IpAddresses, sbtsv/ITsSbTargetEx::IpAddresses, sbtsv/ITsSbTargetEx::get_IpAddresses, sbtsv/ITsSbTargetEx::put_IpAddresses, termserv.itssbtarget_ipaddresses
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbTarget::put_IpAddresses
 - sbtsv/ITsSbTarget::put_IpAddresses
dev_langs:
 - c++
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
---

# ITsSbTarget::put_IpAddresses


## -description

 Retrieves or specifies the external IP addresses of the target.

This property is read/write.

## -parameters

## -remarks

This property was formerly known as <b>TargetExternalIpAddresses</b> in Windows Server 2008 R2.

If the number of external IP addresses is unknown, you can call this method with <i>sockaddr</i> set to <b>NULL</b>. The method will then return, in the <i>numAddresses</i> parameter, the number of <a href="/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint">TSSD_ConnectionPoint</a> structures necessary to receive all the external IP addresses. Allocate the array for <i>sockaddr</i> based on this number, and then call the method again, setting <i>sockaddr</i> to the newly allocated array and <i>numAddresses</i> to the number returned by the first call.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>



<a href="/windows/desktop/TermServ/itssbtargetex">ITsSbTargetEx</a>



<a href="/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint">TSSD_ConnectionPoint</a>
