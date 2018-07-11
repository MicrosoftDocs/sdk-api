---
UID: NF:devicetopology.IPerChannelDbLevel.SetLevelUniform
title: IPerChannelDbLevel::SetLevelUniform
author: windows-sdk-content
description: The SetLevelUniform method sets all channels in the audio stream to the same uniform volume level, in decibels.
old-location: coreaudio\iperchanneldblevel_setleveluniform.htm
old-project: CoreAudio
ms.assetid: b78bebcb-d32b-4eda-a805-35d4459b6b4f
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: IPerChannelDbLevel interface [Core Audio],SetLevelUniform method, IPerChannelDbLevel.SetLevelUniform, IPerChannelDbLevel::SetLevelUniform, IPerChannelDbLevelSetLevelUniform, SetLevelUniform, SetLevelUniform method [Core Audio], SetLevelUniform method [Core Audio],IPerChannelDbLevel interface, coreaudio.iperchanneldblevel_setleveluniform, devicetopology/IPerChannelDbLevel::SetLevelUniform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: devicetopology.h
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
tech.root: 
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPerChannelDbLevel.SetLevelUniform
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPerChannelDbLevel::SetLevelUniform


## -description



The <b>SetLevelUniform</b> method sets all channels in the audio stream to the same uniform volume level, in decibels.




## -parameters




### -param fLevelDB [in]

The new uniform level in decibels.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a2f32cb9-3c8b-4b44-96a2-dd70afcca71a">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetLevelUniform</b> call changes the state of the level control, all clients that have registered <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



If the specified uniform level is beyond the range that the <a href="https://msdn.microsoft.com/492eddb0-f8f2-4639-b5fe-1d02bf8c983a">IPerChannelDbLevel::GetLevelRange</a> method reports for a particular channel, the <b>SetLevelUniform</b> call clamps the value for that channel to the supported range and completes successfully. A subsequent call to the <a href="https://msdn.microsoft.com/afc76c80-1656-4f06-8024-c9b041f52e64">IPerChannelDbLevel::GetLevel</a> method retrieves the actual value used for that channel.




## -see-also




<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>



<a href="https://msdn.microsoft.com/afc76c80-1656-4f06-8024-c9b041f52e64">IPerChannelDbLevel::GetLevel</a>



<a href="https://msdn.microsoft.com/492eddb0-f8f2-4639-b5fe-1d02bf8c983a">IPerChannelDbLevel::GetLevelRange</a>
 

 

