---
UID: NF:rtscom.IStylusPlugin.Error
title: IStylusPlugin::Error
author: windows-sdk-content
description: Notifies the implementing object that this plug-in or one of the previous plug-ins in either the IStylusAsyncPlugin or IStylusSyncPlugin collection threw an exception.
old-location: tablet\istylusplugin_error.htm
old-project: tablet
ms.assetid: 236589f8-a6ae-4db3-8be4-68c5babeb9f0
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 236589f8-a6ae-4db3-8be4-68c5babeb9f0, Error, Error method [Tablet PC], Error method [Tablet PC],IStylusPlugin interface, IStylusPlugin interface [Tablet PC],Error method, IStylusPlugin.Error, IStylusPlugin::Error, rtscom/IStylusPlugin::Error, tablet.istylusplugin_error
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusPlugin.Error
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStylusPlugin::Error


## -description



Notifies the implementing object that this plug-in or one of the previous plug-ins in either the <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> or <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> collection threw an exception.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param piPlugin [in]

The <a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin</a> object that sent the notification.


### -param dataInterest [in]

Identifier of the <a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin</a> method that generated the error.


### -param hrErrorCode [in]

The <b>HRESULT</b> code for the error that occurred.


### -param lptrKey [in, out]

Used internally by the system.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/712908e1-2d1d-4e42-8c80-71354b03d318">Classes and Interfaces - Ink Analysis</a>.




## -remarks



This method is called when the RTS object has caught an exception.


#### Examples

The following C++ example implements an <b>IStylusPlugin::Error Method</b> method that outputs a message and error code to the debug window using <a href="http://go.microsoft.com/fwlink/p/?linkid=73729">The TRACE Macro</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CPacketModifier::Error( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ IStylusPlugin *piPlugin,
            /* [in] */ RealTimeStylusDataInterest dataInterest,
            /* [in] */ HRESULT hrErrorCode,
            /* [out][in] */ LONG_PTR *lptrKey)
{
	CString strError;
	strError.Format(L"An error occurred. Error code: %d", hrErrorCode);
	TRACE(strError);
	return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/7ff6ccf2-292c-4321-be2a-d6db7ce14943">IStylusPlugin::DataInterest Method</a>
 

 

