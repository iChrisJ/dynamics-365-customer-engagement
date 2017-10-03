---
title: "Form properties (Dynamics 365 Customer Engagement) | MicrosoftDocs"
ms.custom: ""
ms.date: 09/30/2017
ms.reviewer: ""
ms.service: "crm-online"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 4ed30bb7-dca1-4de8-80f3-842152ea921a
caps.latest.revision: 63
ms.author: "rdubois"
manager: "brycho"
---
# Form properties 

[!INCLUDE[cc-applies-to-update-9-0-0](../includes/cc_applies_to_update_9_0_0.md)]

 The following table lists the form properties for Dynamics 365 Customer Engagement forms:  
  
|Tab|Property|Description|  
|---------|--------------|-----------------|  
|**Events**|**Form Libraries**|Manage which [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources are available in the form and the order in which they will be loaded.|  
||**Event Handers**|Configure which [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] functions from the Form Libraries will run for the `OnLoad` and `OnSave` form events and the order in which they’ll be run.|  
|**Display**|**Form Name**|Enter a name that will be meaningful to people. This name will be shown to people when they use the form. If they can use multiple forms configured for the entity they will use this name to differentiate between available forms.|  
||**Description**|Enter a description that explains how this form is different from other main forms. This description is only shown in the list of forms for an entity in the solution explorer.|  
||**Page Navigation**|You can choose not to show navigation items.<br /><br /> In forms for updated entities this means the primary name value for the record currently being viewed will not appear in the navigation bar to allow navigation to associated views.<br /><br /> In forms using the classic presentation, the navigation options to choose associated views on the left side of the form will not be shown.|  
||**Image**|When an entity has an image field and the entities’ **Primary Image** option is set, this setting will enable showing the image field in the header of this form.<br /><br /> See [Enable or disable entity options](edit-entities.md#enable-or-disable-entity-options) for more information about entity options.|  ||**Display**|**Set a Max Width (in pixels)** to limit the width of the form. The default value is 1900.|  
|**Parameters**|**Parameters**|Each form can be opened with code using a URL. The URL may also contain data that can be passed to the form using a query string that is appended to the URL. Query strings look like this example:<br />`?p_firstName=Jim&p_lastName=Daly`<br /><br /> As a security measure, forms will not accept any unknown query string parameters. Use this parameters list to specify parameters this form should accept to support code that will pass data to the forms using a query string.<br /><br /> The name and type of data will be checked and the form won’t open if invalid query string parameters are passed to it.><br /><br />**Note:** The name cannot start with an underscore (_) or crm\_. It must start with alphanumeric  characters followed by an underscore (\_). For example, parameter_1 or 1_parameter. The name cannot contain hyphens (-), colons (:), semicolons (;), commas (,) or periods (.). <br /><br />|  
|**Non-Event Dependencies**|**Dependent Fields**|Each event handler has a similar **Dependent Fields** property so that any fields that are needed by the script can be registered. Anyone who tries to remove the dependent fields will not be able to.<br /><br /> Some scripts operate on the form but are not configured in an event handler. Scripts that are initiated from the command bar do not have a place where dependent fields can be registered. This form property provides a place for dependent fields for those scripts to be registered.|  