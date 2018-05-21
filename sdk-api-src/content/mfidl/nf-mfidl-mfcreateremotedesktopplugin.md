---
UID: NF:mfidl.MFCreateRemoteDesktopPlugin
title: MFCreateRemoteDesktopPlugin function
author: windows-driver-content
description: Creates the remote desktop plug-in object. Use this object if the application is running in a Terminal Services client session.
old-location: mf\mfcreateremotedesktopplugin.htm
old-project: medfound
ms.assetid: c986c80b-b583-47be-91e7-5881db0018c2
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MFCreateRemoteDesktopPlugin, MFCreateRemoteDesktopPlugin function [Media Foundation], c986c80b-b583-47be-91e7-5881db0018c2, mf.mfcreateremotedesktopplugin, mfidl/MFCreateRemoteDesktopPlugin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateRemoteDesktopPlugin
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateRemoteDesktopPlugin function


## -description



Creates the remote desktop plug-in object. Use this object if the application is running in a Terminal Services client session.




## -parameters




### -param ppPlugin

Receives a pointer to the <a href="https://msdn.microsoft.com/75bb9bf8-12a7-430f-9943-18623aff9903">IMFRemoteDesktopPlugin</a> interface of the plug-in object. The caller must release the interface.


## -returns




            The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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

                The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Remote desktop connections are not allowed by the current session policy.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

