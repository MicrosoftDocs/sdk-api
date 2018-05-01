---
UID: NS:tcpestats._TCP_ESTATS_OBS_REC_ROD_v0
title: "_TCP_ESTATS_OBS_REC_ROD_v0"
author: windows-driver-content
description: Contains read-only dynamic information for extended TCP statistics observed on the remote receiver for a TCP connection.
old-location: iphlp\tcp_estats_obs_rec_rod_v0.htm
old-project: IpHlp
ms.assetid: f790e107-0db3-4691-98fc-378518b04a8a
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PTCP_ESTATS_OBS_REC_ROD_v0, PTCP_ESTATS_OBS_REC_ROD_v0, PTCP_ESTATS_OBS_REC_ROD_v0 structure pointer [IP Helper], TCP_ESTATS_OBS_REC_ROD_v0, TCP_ESTATS_OBS_REC_ROD_v0 structure [IP Helper], _TCP_ESTATS_OBS_REC_ROD_v0, iphlp.tcp_estats_obs_rec_rod_v0, tcpestats/PTCP_ESTATS_OBS_REC_ROD_v0, tcpestats/TCP_ESTATS_OBS_REC_ROD_v0"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tcpestats.h
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
req.typenames: TCP_ESTATS_OBS_REC_ROD_v0, *PTCP_ESTATS_OBS_REC_ROD_v0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tcpestats.h
api_name:
-	TCP_ESTATS_OBS_REC_ROD_v0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _TCP_ESTATS_OBS_REC_ROD_v0 structure


## -description


The <b>TCP_ESTATS_OBS_REC_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics observed on the remote receiver for a TCP connection.


## -struct-fields




### -field CurRwinRcvd

Type: <b>ULONG</b>

The most recent window advertisement, in bytes, received from the remote receiver.


### -field MaxRwinRcvd

Type: <b>ULONG</b>

The maximum window advertisement, in bytes, received from the remote receiver.


### -field MinRwinRcvd

Type: <b>ULONG</b>

The minimum window advertisement, in bytes, received from the remote receiver.


### -field WinScaleRcvd

Type: <b>ULONG</b>

The value of the received window scale option if one was
           received from the remote receiver; otherwise, a value of -1.

Note that if both the <b>WinScaleSent</b> member of the  <a href="https://msdn.microsoft.com/1481f108-1ea3-4952-9131-8b15e373d83e">TCP_ESTATS_REC_ROD_v0</a> structure  and
           the <b>WinScaleRcvd</b> member are not -1, then Snd.Wind.Scale
           will be the same as this value and used to scale receiver
           window announcements from the remote host to the local
           host.


## -remarks



The <b>TCP_ESTATS_OBS_REC_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_OBS_REC_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information for extended TCP statistics on the local receiver for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_OBS_REC_ROD_v0</b> structure is retrieved by calls to  the <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> or <a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsObsRec</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=121686">http://www.ietf.org/rfc/rfc4898.txt</a>.




The following is the mapping of the members in the <b>TCP_ESTATS_OBS_REC_ROD_v0</b> structure to the entries defined in RFC 4898 for extended TCP statistics:



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="CurRwinRcvd"></a><a id="currwinrcvd"></a><a id="CURRWINRCVD"></a><b>CurRwinRcvd</b>

</td>
<td width="60%">
tcpEStatsPerfCurRwinRcvd

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxRwinRcvd"></a><a id="maxrwinrcvd"></a><a id="MAXRWINRCVD"></a><b>MaxRwinRcvd</b>

</td>
<td width="60%">
tcpEStatsPerfMaxRwinRcvd

</td>
</tr>
<tr>
<td width="40%">
<a id="MinRwinRcvd"></a><a id="minrwinrcvd"></a><a id="MINRWINRCVD"></a><b>MinRwinRcvd</b>

</td>
<td width="60%">
No mapping to this member.

</td>
</tr>
<tr>
<td width="40%">
<a id="WinScaleRcvd"></a><a id="winscalercvd"></a><a id="WINSCALERCVD"></a><b>WinScaleRcvd</b>

</td>
<td width="60%">
tcpEStatsStackWinScaleRcvd

</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

