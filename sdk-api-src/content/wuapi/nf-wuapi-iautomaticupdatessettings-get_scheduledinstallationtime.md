---
UID: NF:wuapi.IAutomaticUpdatesSettings.get_ScheduledInstallationTime
title: IAutomaticUpdatesSettings::get_ScheduledInstallationTime (wuapi.h)
description: Gets and sets the time at which Automatic Updates installs or uninstalls updates. (Get)
helpviewer_keywords: ["IAutomaticUpdatesSettings interface [Windows Update Agent]","ScheduledInstallationTime property","IAutomaticUpdatesSettings.ScheduledInstallationTime","IAutomaticUpdatesSettings.get_ScheduledInstallationTime","IAutomaticUpdatesSettings::ScheduledInstallationTime","IAutomaticUpdatesSettings::get_ScheduledInstallationTime","IAutomaticUpdatesSettings::put_ScheduledInstallationTime","ScheduledInstallationTime property [Windows Update Agent]","ScheduledInstallationTime property [Windows Update Agent]","IAutomaticUpdatesSettings interface","get_ScheduledInstallationTime","wua.iautomaticupdatessettings_scheduledinstallationtime","wuapi/IAutomaticUpdatesSettings::ScheduledInstallationTime","wuapi/IAutomaticUpdatesSettings::get_ScheduledInstallationTime","wuapi/IAutomaticUpdatesSettings::put_ScheduledInstallationTime"]
old-location: wua\iautomaticupdatessettings_scheduledinstallationtime.htm
tech.root: wua
ms.assetid: 1b1adefc-785e-46ad-8984-d2beb1c2202c
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings interface [Windows Update Agent],ScheduledInstallationTime property, IAutomaticUpdatesSettings.ScheduledInstallationTime, IAutomaticUpdatesSettings.get_ScheduledInstallationTime, IAutomaticUpdatesSettings::ScheduledInstallationTime, IAutomaticUpdatesSettings::get_ScheduledInstallationTime, IAutomaticUpdatesSettings::put_ScheduledInstallationTime, ScheduledInstallationTime property [Windows Update Agent], ScheduledInstallationTime property [Windows Update Agent],IAutomaticUpdatesSettings interface, get_ScheduledInstallationTime, wua.iautomaticupdatessettings_scheduledinstallationtime, wuapi/IAutomaticUpdatesSettings::ScheduledInstallationTime, wuapi/IAutomaticUpdatesSettings::get_ScheduledInstallationTime, wuapi/IAutomaticUpdatesSettings::put_ScheduledInstallationTime
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAutomaticUpdatesSettings::get_ScheduledInstallationTime
 - wuapi/IAutomaticUpdatesSettings::get_ScheduledInstallationTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdatesSettings.ScheduledInstallationTime
 - IAutomaticUpdatesSettings.get_ScheduledInstallationTime
 - IAutomaticUpdatesSettings.put_ScheduledInstallationTime
---

# IAutomaticUpdatesSettings::get_ScheduledInstallationTime


## -description

<p class="CCE_Message">[<b>IAutomaticUpdatesSettings::ScheduledInstallationTime</b> is no longer supported as of Windows 10.]


Gets and sets the time at which Automatic Updates  installs or uninstalls updates.



This property is read/write.

## -parameters

## -remarks

The time is set by using the following values.

<table>
<tr>
<th>Value</th>
<th>Time</th>
</tr>
<tr>
<td>0</td>
<td>00:00</td>
</tr>
<tr>
<td>1</td>
<td>01:00</td>
</tr>
<tr>
<td>2</td>
<td>02:00</td>
</tr>
<tr>
<td>3</td>
<td>03:00</td>
</tr>
<tr>
<td>4</td>
<td>04:00</td>
</tr>
<tr>
<td>5</td>
<td>05:00</td>
</tr>
<tr>
<td>6</td>
<td>06:00</td>
</tr>
<tr>
<td>7</td>
<td>07:00</td>
</tr>
<tr>
<td>8</td>
<td>08:00</td>
</tr>
<tr>
<td>9</td>
<td>09:00</td>
</tr>
<tr>
<td>10</td>
<td>10:00</td>
</tr>
<tr>
<td>11</td>
<td>11:00</td>
</tr>
<tr>
<td>12</td>
<td>12:00</td>
</tr>
<tr>
<td>13</td>
<td>13:00</td>
</tr>
<tr>
<td>14</td>
<td>14:00</td>
</tr>
<tr>
<td>15</td>
<td>15:00</td>
</tr>
<tr>
<td>16</td>
<td>16:00</td>
</tr>
<tr>
<td>17</td>
<td>17:00</td>
</tr>
<tr>
<td>18</td>
<td>18:00</td>
</tr>
<tr>
<td>19</td>
<td>19:00</td>
</tr>
<tr>
<td>20</td>
<td>20:00</td>
</tr>
<tr>
<td>21</td>
<td>21:00</td>
</tr>
<tr>
<td>22</td>
<td>22:00</td>
</tr>
<tr>
<td>23</td>
<td>23:00</td>
</tr>
</table>
 

The value of this property is ignored if the value of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">NotificationLevel</a> property is not <b>aunlScheduledInstallation</b>. 

<div class="alert"><b>Note</b>  Starting with Windows 8 and Windows Server 2012, <b>ScheduledInstallationTime</b> is not supported and will return unreliable values. If you try to modify <b>ScheduledInstallationTime</b>, the operation will appear to succeed but will have no effect.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a>
